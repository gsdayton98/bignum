cmake_minimum_required(VERSION 4.4)
project(bignumber)

set(CMAKE_CXX_STANDARD 23)

add_library(bignumber SHARED library.cpp
        src/dynamic_array.cpp
        include/bignumber/dynamic_array.hpp)
