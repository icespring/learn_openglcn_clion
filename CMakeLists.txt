cmake_minimum_required(VERSION 3.10)
project(learn_opengl)

set(CMAKE_CXX_STANDARD 11)
include_directories(${CMAKE_SOURCE_DIR}/include)

#link_directories(/usr/local/Cellar/glfw/3.2.1/lib)
find_library(glfw3 glfw)

add_executable(learn_opengl
        glad.c
        include/learnopengl/shader_m.h
        include/stb_image.h
        include/learnopengl/camera.h
#        f01_0402_texture_combined.cpp
#        f01_0501_transformations.cpp
#        f01_0601_coordinate_systems.cpp
#        f01_0602_coordinate_systems_depth.cpp
#        f01_0603_coordinate_systems_multiple.cpp
#        f01_0701_camera_circle.cpp
#        f01_0702_camera_keyboard_dt.cpp
#        f01_0703_camera_mouse_zoom.cpp
        f01_0704_camera_class.cpp)

target_link_libraries(learn_opengl ${glfw3})

#target_link_libraries(LibsModule -L/usr/local/Cellar/glfw/3.2.1/lib)
