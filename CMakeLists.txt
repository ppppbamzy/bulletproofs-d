cmake_minimum_required(VERSION 3.14)

project(bulletproofs LANGUAGES CXX)

# require C++14
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(src)
add_subdirectory(src)

option(BULLETPROOFS_ENABLE_TESTS OFF)
if(BULLETPROOFS_ENABLE_TESTS)
    ENABLE_TESTING()
    add_subdirectory(tests)
endif()
