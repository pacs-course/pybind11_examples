cmake_minimum_required(VERSION 3.0.0)
project(example)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED On)
set(CMAKE_CXX_EXTENSIONS Off)
set(CMAKE_VERBOSE_MAKEFILE ON)
find_package(Eigen3 REQUIRED HINTS $ENV{mkEigenPrefix})
include_directories(SYSTEM ${EIGEN3_INCLUDE_DIRS})

find_package(pybind11 REQUIRED HINTS $ENV{mkPybind11Prefix})
include_directories(SYSTEM ${pybind11_INCLUDE_DIRS})

pybind11_add_module(example example.cpp)

