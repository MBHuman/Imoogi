# ABOUT PROJECT
# This project is unorderd extandable database for store, search, process data

# --- Cmake settings ----------------------------------------------------------

# cmake version
cmake_minimum_required(VERSION 3.11)

# set c++ standard
set(CMAKE_CXX_STANDARD 17)

# --- Project information -----------------------------------------------------

# project name
project(imoogi CXX)

# --- Project main part  ------------------------------------------------------

# project's source files
add_subdirectory(src)

# main executable program
add_executable(${PROJECT_NAME} src/main.cpp)

# --- Tests -------------------------------------------------------------------

# project's tests
add_subdirectory(tests)

# googletest lib for testing cpp

# --- External libraries ------------------------------------------------------

# include ctest or include from gtest source code
include(CTest)
if(NOT gtest_FOUND)
    message("Google test not installed, use it's source code from external folder!!!")
    add_subdirectory(3rd_party/gtest)
endif(NOT gtest_FOUND)
