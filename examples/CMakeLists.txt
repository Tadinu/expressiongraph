IF(ENABLE_EXAMPLES)
  set(EXAMPLES
    geometry.cpp
    expressiontree_example.cpp
    expressiontree_example2.cpp
    expressiontree_example3.cpp
    expressiontree_example4.cpp
    expressiontree_example5.cpp
    expressiontree_example6.cpp
    expressiontree_example7.cpp
    expressiontree_example8.cpp
    expressiontree_example9.cpp
    expressiontree_example10.cpp
    expressiontree_example11.cpp
    expressiontree_example12.cpp
    resolved_motion_rate_control.cpp
    expressiontree_perpendicular.cpp
    conversions_example.cpp
    expressiontree_distance_to_line.cpp
    expressiontree_conditional.cpp
    expressiontree_cached_named.cpp
    expressiontree_optimizer.cpp
    expressiontree_mimo_ex.cpp
    expressiontree_sensor.cpp
    expressiontree_motion_profile.cpp
    expressiontree_motion_profile2.cpp
    expressiontree_variabletype.cpp
    tutorial1.cpp
    tutorial2.cpp
    tutorial3.cpp
    saturate.cpp
    debug1.cpp
    matrix_traits.cpp
    initial_value.cpp
    mptrap_tst.cpp
    solving_and_cloning.cpp
  )

  add_executable(solving_and_cloning solving_and_cloning.cpp )
  TARGET_LINK_LIBRARIES(solving_and_cloning ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(mptrap_tst mptrap_tst.cpp )
  TARGET_LINK_LIBRARIES(mptrap_tst ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(matrix_traits matrix_traits.cpp )
  TARGET_LINK_LIBRARIES(matrix_traits ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(geometry geometry.cpp )
  TARGET_LINK_LIBRARIES(geometry ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_variabletype expressiontree_variabletype.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_variabletype ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_example expressiontree_example.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example ${PROJECT_NAME} ${Eigen_LIBRARIES})
 
  add_executable(expressiontree_example2 expressiontree_example2.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example2 ${PROJECT_NAME} ${Eigen_LIBRARIES})
 
  add_executable(expressiontree_example3 expressiontree_example3.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example3 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_example4 expressiontree_example4.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example4 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_example5 expressiontree_example5.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example5 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_example6 expressiontree_example6.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example6 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_example7 expressiontree_example7.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example7 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_example8 expressiontree_example8.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example8 ${PROJECT_NAME} ${Eigen_LIBRARIES})
 
  add_executable(expressiontree_example9 expressiontree_example9.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example9 ${PROJECT_NAME} ${Eigen_LIBRARIES}) 
  add_executable(expressiontree_example10 expressiontree_example10.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example10 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_example11 expressiontree_example11.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example11 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_example12 expressiontree_example12.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_example12 ${PROJECT_NAME} ${Eigen_LIBRARIES})
 
  #add_executable(expressiontree_example13 expressiontree_example13.cpp )
  #TARGET_LINK_LIBRARIES(expressiontree_example13 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(resolved_motion_rate_control resolved_motion_rate_control.cpp )
  TARGET_LINK_LIBRARIES(resolved_motion_rate_control  ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_perpendicular expressiontree_perpendicular.cpp )
  TARGET_LINK_LIBRARIES(expressiontree_perpendicular  ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(conversions_example conversions_example.cpp )
  TARGET_LINK_LIBRARIES(conversions_example ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_distance_to_line  expressiontree_distance_to_line.cpp)
  TARGET_LINK_LIBRARIES(expressiontree_distance_to_line ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_conditional  expressiontree_conditional.cpp)
  TARGET_LINK_LIBRARIES(expressiontree_conditional ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_cached_named expressiontree_cached_named.cpp)
  TARGET_LINK_LIBRARIES(expressiontree_cached_named ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_optimizer expressiontree_optimizer.cpp)
  TARGET_LINK_LIBRARIES(expressiontree_optimizer ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_mimo_ex expressiontree_mimo_ex.cpp)
  TARGET_LINK_LIBRARIES(expressiontree_mimo_ex ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_sensor expressiontree_sensor.cpp)
  TARGET_LINK_LIBRARIES(expressiontree_sensor ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_motion_profile expressiontree_motion_profile.cpp)
  TARGET_LINK_LIBRARIES(expressiontree_motion_profile ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(expressiontree_motion_profile2 expressiontree_motion_profile2.cpp)
  TARGET_LINK_LIBRARIES(expressiontree_motion_profile2 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(initial_value initial_value.cpp)
  TARGET_LINK_LIBRARIES(initial_value ${PROJECT_NAME} ${Eigen_LIBRARIES})

  # TUTORIAL FILES:
  add_executable(tutorial1 tutorial1.cpp)
  TARGET_LINK_LIBRARIES(tutorial1 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(tutorial2 tutorial2.cpp)
  TARGET_LINK_LIBRARIES(tutorial2 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(tutorial3 tutorial3.cpp)
  TARGET_LINK_LIBRARIES(tutorial3 ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(saturate saturate.cpp)
  TARGET_LINK_LIBRARIES(saturate ${PROJECT_NAME} ${Eigen_LIBRARIES})

  add_executable(debug1 debug1.cpp)
  TARGET_LINK_LIBRARIES(debug1 ${PROJECT_NAME} ${Eigen_LIBRARIES})
ENDIF(ENABLE_EXAMPLES)  

