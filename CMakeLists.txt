cmake_minimum_required(VERSION 3.6)
project(OpenGL)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
include_directories(${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS})



set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
add_compile_options("-lglut -lGLU -lGL")

set(SOURCE_FILES main.cpp)
add_executable(OpenGL ${SOURCE_FILES})
target_link_libraries(OpenGL ${OPENGL_LIBRARIES} ${GLUT_LIBRARIES})