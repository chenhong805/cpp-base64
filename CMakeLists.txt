cmake_minimum_required(VERSION 3.5)
project(cpp_base64)

add_library(libbase64 base64.cpp base64.h)
target_include_directories(libbase64 PUBLIC "${CMAKE_CURRENT_LIST_DIR}")

add_executable(testcpp test.cpp)
target_link_libraries(testcpp libbase64)
add_test(NAME testcpp
         COMMAND testcpp
         )

