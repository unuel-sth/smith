cmake_minimum_required(VERSION 3.25)
project(smith VERSION 0.1)
add_executable(smith src/main.cpp)
set(CMAKE_CXX_STANDARD 23)

add_subdirectory(src/display)

include_directories(src/display 
    src/display/external/glad/include
    src/display/external/glfw/include)

target_link_libraries(smith PUBLIC glad display)