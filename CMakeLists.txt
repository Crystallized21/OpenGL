cmake_minimum_required(VERSION 3.15)
project(OpenGL)

set(CMAKE_CXX_STANDARD 20)

find_package(glfw3 REQUIRED)

find_package(OpenGL REQUIRED)

add_compile_definitions(GL_SILENCE_DEPRECATION)

add_executable(${PROJECT_NAME} src/main.cpp)

target_link_libraries(${PROJECT_NAME}
    PRIVATE
    glfw
    ${OPENGL_LIBRARIES}
)