# only for cmake --version >= 3.5.1
cmake_minimum_required(VERSION 3.27)

# project name
project(rvarago_hello_cmake)

# creates the variable EXEC and sets it to hello
set(EXEC hello)

# set the C++14 standard
set(CMAKE_CXX_STANDARD 14)

set(CMAKE_C_COMPILER /usr/bin/arm-linux-gnueabi-gcc)
set(CMAKE_CXX_COMPILER /usr/bin/arm-linux-gnueabi-g++)
set(CMAKE_FIND_ROOT_PATH_MODE_PROGRAM NEVER)
set(CMAKE_FIND_ROOT_PATH_MODE_LIBRARY ONLY)
set(CMAKE_FIND_ROOT_PATH_MODE_INCLUDE ONLY)
set(CMAKE_FIND_ROOT_PATH_MODE_PACKAGE ONLY)

# I../includes
include_directories(includes)

# puts all .cpp files inside src to the SOURCES variable
file(GLOB SOURCES src/*.cpp)

# compiles the files defined by SOURCES to generante the executable defined by EXEC
add_executable(${EXEC} ${SOURCES})
#add_executable(rvarago_hello_cmake_ src/main.cpp
#        src/person.cpp
#        includes/person.hpp
#)
