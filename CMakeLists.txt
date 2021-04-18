cmake_minimum_required(VERSION 3.18)

project(Hash_map)

if (CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)
    include(CTest)
endif ()


add_library(Hash_map INTERFACE)

target_compile_features(Hash_map INTERFACE cxx_std_20)

target_include_directories(Hash_map INTERFACE "include")


if (CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME AND BUILD_TESTING)
    add_subdirectory(tests)
endif ()
