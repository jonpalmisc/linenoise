cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

project(linenoise LANGUAGES C)

add_library(linenoise linenoise.h linenoise.c)
target_compile_features(linenoise PRIVATE c_std_99)
target_include_directories(linenoise PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

install(TARGETS linenoise)
install(FILES linenoise.h TYPE INCLUDE)
