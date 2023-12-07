cmake_minimum_required(VERSION 3.26)
project(game_of_life C)

set(CMAKE_C_STANDARD 11)

add_executable(game_of_life
        main.c
)

find_package(glfw3 3.3 REQUIRED)
target_link_libraries(game_of_life glfw)
find_package(OpenGL REQUIRED)
target_link_libraries(game_of_life OpenGL::GL)
