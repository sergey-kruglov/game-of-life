cmake_minimum_required(VERSION 3.26)
project(testc C)

set(CMAKE_C_STANDARD 11)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_executable(testc
        main.c
)

add_subdirectory(vendor/glfw-3.3.8)
target_link_libraries(testc glfw)

find_package(OpenGL REQUIRED)
target_link_libraries(testc OpenGL::GL)
