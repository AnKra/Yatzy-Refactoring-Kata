cmake_minimum_required(VERSION 3.16)
set(CMAKE_VERBOSE_MAKEFILE ON)
project(Yatzy VERSION 1.0
        LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 17)
# uncomment these lines to enable coverage measurements using gcov
#set(CMAKE_CXX_FLAGS "--coverage")

set (CMAKE_CXX_FLAGS "-Wno-maybe-uninitialized")  # ignore warning to prevent compiler error related to gtest

enable_testing()
add_subdirectory(src)
add_subdirectory(test-doctest)
add_subdirectory(test-gtest)

