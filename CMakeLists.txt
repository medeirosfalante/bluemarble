cmake_minimum_required(VERSION 3.0.0)
project(BlueMarble VERSION 0.0.1)

add_executable(${PROJECT_NAME} main.cpp)

find_package(glfw3 REQUIRED)
find_package(GLEW REQUIRED)
find_package(OpenGL REQUIRED)

target_include_directories(${PROJECT_NAME} PRIVATE deps/glm deps/stb deps/glfw/include)

target_link_libraries(${PROJECT_NAME}  GLEW::glew glfw OpenGL::OpenGL)