cmake_minimum_required(VERSION 3.13)

project (hello_emscripten)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_EXECUTABLE_SUFFIX ".html")
set (SOURCE_FILES hello.cpp)

add_executable(index ${SOURCE_FILES})
