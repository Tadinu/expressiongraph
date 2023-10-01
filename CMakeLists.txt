cmake_minimum_required(VERSION 3.5)
project(expressiongraph)

#set the default path for built executables to the "bin" directory
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#set the default path for built libraries to the "lib" directory
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

OPTION(ENABLE_EXAMPLES "enable compilation of a series of examples" ON) 

# Default to C99
if(NOT CMAKE_C_STANDARD)
  set(CMAKE_C_STANDARD 99)

endif()

# Default to C++17
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 17)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(ament_cmake REQUIRED)
find_package(ament_index_cpp REQUIRED)

find_package(Eigen3 REQUIRED)
find_package(orocos_kdl REQUIRED)
include_directories(include ${eigen_INCLUDE_DIRS} ${orocos_kdl_INCLUDE_DIRS})

if(ENABLE_EXAMPLES)
  add_subdirectory(examples)
endif()

set(EXPRESSIONTREE_SRCS
  src/expressiontree_chain.cpp
  src/expressiontree_double.cpp
  src/expressiontree_expressions.cpp
  src/expressiontree_frame.cpp
  src/expressiontree_mimo.cpp
  src/expressiontree_motionprofiles.cpp
  #src/expressiontree_motprof.cpp.bak
  src/expressiontree_rotation.cpp
  src/expressiontree_twist.cpp
  src/expressiontree_vector.cpp
  src/expressiontree_wrench.cpp
  src/mptrap.cpp
)

add_library(${PROJECT_NAME} ${EXPRESSIONTREE_SRCS})
target_include_directories(${PROJECT_NAME} PUBLIC ${orocos_kdl_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} ${orocos_kdl_LIBRARIES})

#############
## Testing ##
#############

if (BUILD_TESTING)
  find_package(ament_cmake_gtest REQUIRED)
  ament_add_gtest(${PROJECT_NAME}-test tests/expressiongraph_test.cpp)
  target_link_libraries(${PROJECT_NAME}-test ${PROJECT_NAME})
endif()

install(TARGETS ${PROJECT_NAME}
  ARCHIVE DESTINATION lib
  LIBRARY DESTINATION lib
  RUNTIME DESTINATION bin
)

install(
  DIRECTORY include/
  DESTINATION include
)

# Export dependencies, include for downstream/client CMake-based packages
ament_export_dependencies()
ament_export_include_directories(include)
ament_export_libraries(${PROJECT_NAME})
ament_package()
 
