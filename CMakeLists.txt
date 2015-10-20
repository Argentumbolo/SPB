cmake_minimum_required (VERSION 2.8)

set (PRJ "spb")
set ("${PRJ}_BIN_DIR" bin)
set ("${PRJ}_SRC_DIR" src)
set (EXECUTABLE_OUTPUT_PATH ${${PRJ}_BIN_DIR})

set (CMAKE_VERBOSE_MAKEFILE ON)
set (CMAKE_BUILD_TYPE Debug)

if (CMAKE_COMPILER_IS_GNUCC)
    set (CMAKE_C_FLAGS "-O0")
    set (CMAKE_C_FLAGS "-std=c11")
endif (CMAKE_COMPILER_IS_GNUCC)

if (MSVC)
    set (CMAKE_C_FLAGS "/Od")
endif (MSVC)

set (MAIN_SRC ${${PRJ}_SRC_DIR}/Source.c)
add_executable (${PRJ} ${MAIN_SRC})
