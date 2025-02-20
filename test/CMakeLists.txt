find_package(Catch2 REQUIRED)

add_executable(tests tests.cpp)
target_link_libraries(tests PRIVATE Catch2::Catch2WithMain)

add_test(NAME myTest COMMAND tests)

message(STATUS "Tests executable is: ${CMAKE_BINARY_DIR}/tests")