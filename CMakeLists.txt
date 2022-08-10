cmake_minimum_required(VERSION 3.24)

project(learn-glfw CXX)

add_executable(learn-glfw src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(deps/glfw)
add_subdirectory(deps/glew/build/cmake)

include_directories(deps/glew/include)

target_link_libraries(learn-glfw glfw)
target_link_libraries(learn-glfw glew_s)
