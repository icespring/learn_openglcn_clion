cmake_minimum_required(VERSION 3.10)
project(learn_opengl)

set(CMAKE_CXX_STANDARD 11)
include_directories(${CMAKE_SOURCE_DIR}/include)

#link_directories(/usr/local/Cellar/glfw/3.2.1/lib)
find_library(glfw3 glfw)

add_executable(learn_opengl glad.c f01_0301_shader_uniform.cpp)

target_link_libraries(learn_opengl ${glfw3})

#target_link_libraries(LibsModule -L/usr/local/Cellar/glfw/3.2.1/lib)
