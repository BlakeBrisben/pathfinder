cmake_minimum_required(VERSION 4.0)
project(pathfinder)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(glfw3 3.3 REQUIRED)
add_subdirectory(glad)

add_executable(pathfinder src/main.cpp)
target_link_libraries(
    pathfinder PUBLIC
    glfw
    glad
    dl
)
