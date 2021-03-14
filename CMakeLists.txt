cmake_minimum_required(VERSION 3.10)

# set the project name
project(learnopengl)

# specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# add the executable
add_executable(learnopengl main.cpp)

add_subdirectory(glad/)
target_link_libraries(learnopengl glad)

find_package(glfw3 3.3 REQUIRED)
target_link_libraries(learnopengl glfw)
find_package(OpenGL REQUIRED)
target_link_libraries(learnopengl OpenGL::GL  ${CMAKE_DL_LIBS})


