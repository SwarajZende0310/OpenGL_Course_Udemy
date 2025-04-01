cmake_minimum_required(VERSION 3.31.3)

project(
    OpenGL
    VERSION 1.0.0
    LANGUAGES C CXX
)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)

set(ExecutableName OpenGLApp)

add_executable(${ExecutableName}
    ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp
)

target_link_libraries(${ExecutableName} PUBLIC GL GLEW glfw)