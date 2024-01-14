cmake_minimum_required(VERSION 3.27)
project(FluidSimCpp)

set(CMAKE_CXX_STANDARD 23)

add_compile_definitions(GLEW_STATIC)

link_directories(${PROJECT_SOURCE_DIR}/lib)
set(OpenGLLibs glew32s glfw3 opengl32)
include_directories(${PROJECT_SOURCE_DIR}/include)


add_executable(FluidSimCpp main.cpp)

target_link_libraries(FluidSimCpp ${OpenGLLibs})
