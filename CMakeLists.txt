cmake_minimum_required(VERSION 3.25)
project(Smith VERSION 0.1)
add_executable(Smith src/main.cpp)
set(CMAKE_CXX_STANDARD 23)

add_subdirectory(src/display)

include_directories(src/display 
    src/display/external/glad/include
    src/display/external/glfw/include)

target_link_libraries(Smith PUBLIC glad display)