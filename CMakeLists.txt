cmake_minimum_required(VERSION 3.30 FATAL_ERROR)

set(PROJECT_NAME OpengGL2024)
project(${PROJECT_NAME})


add_executable(${PROJECT_NAME} src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(libs/glfw)
target_link_libraries(${PROJECT_NAME} glfw)

add_subdirectory(libs/glad)
target_link_libraries(${PROJECT_NAME} glad)