cmake_minimum_required(VERSION 3.12)
project(ini_reader_project LANGUAGES C CXX)

add_library(inireader_cpp_shared SHARED
        ${CMAKE_CURRENT_SOURCE_DIR}/cpp/INIReader.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/ini.c
        )
target_include_directories(inireader_cpp_shared
        PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/cpp/
        )
add_library(ini_c_shared SHARED
        ${CMAKE_CURRENT_SOURCE_DIR}/ini.c
        )
target_include_directories(ini_c_shared
        PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/
        )

add_library(inireader_cpp_static STATIC
        ${CMAKE_CURRENT_SOURCE_DIR}/cpp/INIReader.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/ini.c
        )
target_include_directories(inireader_cpp_static
        PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/cpp/
        )
add_library(ini_c_static STATIC
        ${CMAKE_CURRENT_SOURCE_DIR}/ini.c
        )
target_include_directories(ini_c_static
        PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/
        )