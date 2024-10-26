cmake_minimum_required(VERSION 3.29)
project(3Dtesting)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_LIST_DIR}/cmake_modules)

#sdl2
set(SDL2_PATH "../3Dtesting/externalLibs/SLD2-2.28.5-mingw/x86_64-w64-mingw32")

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIR})

add_executable(3Dtesting main.cpp)
target_link_libraries(${PROJECT_NAME} ${SDL2_LIBRARY})

add_compile_options(${PROJECT_NAME} -Wall)