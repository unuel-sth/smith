cmake_policy(SET CMP0072 NEW)

find_package(OpenGL REQUIRED)

add_library(display display.h display.cpp)
add_subdirectory(external/glfw)
add_subdirectory(external/glad)
add_subdirectory(callbacks)
include_directories(display ${CMAKE_CURRENT_SOURCE_DIR} ${OPENGL_INCLUDE_DIRS} callbacks external/glfw/include external/glad/include)


target_link_libraries(display ${OPENGL_LIBRARIES} glad glfw display_callbacks)