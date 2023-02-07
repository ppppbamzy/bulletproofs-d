macro(add_test_case TEST_NAME)
    add_executable(${TEST_NAME}_test ${TEST_NAME}.cpp)
    target_link_libraries(${TEST_NAME}_test PRIVATE ${PROJECT_NAME})
  	add_test(NAME ${TEST_NAME} COMMAND "${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/${TEST_NAME}_test" WORKING_DIRECTORY "${CMAKE_SOURCE_DIR}/")
endmacro()

add_test_case(demo)
add_test_case(math)
add_test_case(prover)
