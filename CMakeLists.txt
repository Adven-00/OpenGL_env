# CMake OpenGL project

# glad, glfw, glm, stb_image
# Windows 10, VSCode, GCC 8.1.0

cmake_minimum_required(VERSION 3.1)

# name
project(test)

find_package(OpenGL REQUIRED)

# environment
set(OpenGL_env E:/study/Computer/project/OpenGL_env)

# source file
add_executable(${PROJECT_NAME} src/main.cpp)

# header file
# target_include_directories(${PROJECT_NAME} PUBLIC ${PROJECT_SOURCE_DIR}/include)

target_include_directories(${PROJECT_NAME} PUBLIC ${OpenGL_env}/include)
target_link_libraries(${PROJECT_NAME} ${OpenGL_env}/lib/libglfw3.a)
target_link_libraries(${PROJECT_NAME} ${OpenGL_env}/lib/libglad.a)
target_link_libraries(${PROJECT_NAME} ${OPENGL_gl_LIBRARY})