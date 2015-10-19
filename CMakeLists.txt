cmake_minimum_required (VERSION 2.8)

set (PRJ "spb")
set ("${PRJ}_BIN_DIR" bin)
set ("${PRJ}_SRC_DIR" src)
set (EXECUTABLE_OUTPUT_PATH ${${PRJ}_BIN_DIR})

set (CMAKE_VERBOSE_MAKEFILE ON)
set (CMAKE_BUILD_TYPE Debug)

set(CMAKE_C_FLAGS "-std=c99")

set (MAIN_SRC ${${PRJ}_SRC_DIR}/Source.c)
add_executable (${PRJ} ${MAIN_SRC})
