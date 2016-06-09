

set(IMGUI_INCLUDE_DIRS ${CMAKE_CURRENT_SOURCE_DIR})
set(IMGUI_INCLUDE_DIRS ${IMGUI_INCLUDE_DIRS} ${CMAKE_CURRENT_SOURCE_DIR}/examples/opengl3_example)
include_directories(${IMGUI_INCLUDE_DIRS})

add_library(imgui imgui.cpp imgui_draw.cpp)
add_library(imgui_demo imgui_demo.cpp)

set(IMGUI_DEMO_LIBRARY imgui_demo PARENT_SCOPE)
set(IMGUI_LIBRARIES imgui PARENT_SCOPE)
set(IMGUI_INCLUDE_DIRS ${IMGUI_INCLUDE_DIRS} PARENT_SCOPE)
