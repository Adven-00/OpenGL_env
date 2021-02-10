# CMake OpenGL project

# glad, glfw, glm, stb_image
# Windows 10, VSCode, GCC 8.1.0

cmake_minimum_required(VERSION 3.1)

# name
project(test)

find_package(OpenGL REQUIRED)

# source file
add_executable(${PROJECT_NAME} src/main.cpp)

# header file
target_include_directories(${PROJECT_NAME} PUBLIC ${PROJECT_SOURCE_DIR}/include)

# library
target_link_libraries(${PROJECT_NAME} ${PROJECT_SOURCE_DIR}/lib/libglfw3.a)
target_link_libraries(${PROJECT_NAME} ${PROJECT_SOURCE_DIR}/lib/libglad.a)
target_link_libraries(${PROJECT_NAME} ${OPENGL_gl_LIBRARY})