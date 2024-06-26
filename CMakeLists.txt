cmake_minimum_required(VERSION 3.10)
project(DentalSlicer)

set(CMAKE_CXX_STANDARD 11) 
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenGL REQUIRED)
find_package(glfw3 3.3 REQUIRED)
find_package(GLEW REQUIRED)
find_package(glm REQUIRED)

add_executable(DentalSlicer main.cpp)

target_include_directories(DentalSlicer PRIVATE ${GLEW_INCLUDE_DIRS} ${GLFW_INCLUDE_DIRS} ${GLM_INCLUDE_DIRS})
target_link_libraries(DentalSlicer ${OPENGL_LIBRARIES} glfw GLEW::GLEW glm)

