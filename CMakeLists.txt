cmake_minimum_required(VERSION 3.13 FATAL_ERROR)

set(PROJECT_NAME BattleCity)
project(${PROJECT_NAME})

add_executable(${PROJECT_NAME}
    src/main.cpp)

set(GLFW_BUILD_EXAMPLES "Build the GLFW example programs" OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS "Build the GLFW test programs" OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_DOCS "Build the GLFW documentation" OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL "Build the GLFW install package" OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${PROJECT_NAME} glfw)

add_subdirectory(external/glad)
target_link_libraries(${PROJECT_NAME} glad)