

set(IMGUI_INCLUDE_DIRS ${CMAKE_CURRENT_SOURCE_DIR})
set(IMGUI_INCLUDE_DIRS ${IMGUI_INCLUDE_DIRS} ${CMAKE_CURRENT_SOURCE_DIR}/examples/opengl3_example)
include_directories(${IMGUI_INCLUDE_DIRS})

add_library(imgui imgui.cpp imgui_draw.cpp)

add_library(imgui_glfw examples/opengl3_example/imgui_impl_glfw_gl3.cpp)
target_link_libraries(imgui imgui_glfw)

set(IMGUI_LIBRARIES imgui PARENT_SCOPE)
set(IMGUI_INCLUDE_DIRS ${IMGUI_INCLUDE_DIRS} PARENT_SCOPE)
