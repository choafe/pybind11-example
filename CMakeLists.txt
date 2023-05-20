cmake_minimum_required(VERSION 3.0.0)
project(example VERSION 0.1.0)

add_subdirectory(extern/pybind11) 

add_executable(example src/main.cpp)

target_include_directories(example PRIVATE extern/pybind11/include)
target_link_libraries(example PRIVATE pybind11::embed)