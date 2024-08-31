cmake_minimum_required(VERSION 3.15)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

if(MSVC)
    add_compile_options(/W4 /WX)
else()
    add_compile_options(-Wall -Wextra -Wpedantic -Werror)
endif()

# Imnodes

add_library(imnodes)
target_sources(imnodes PRIVATE
    imnodes.h
    imnodes_internal.h
    imnodes.cpp)