cmake_minimum_required (VERSION 3.20)

set(IMGUI_DIR ${CMAKE_CURRENT_SOURCE_DIR}/)
add_library(imgui STATIC)
set_property(TARGET imgui PROPERTY CXX_STANDARD 17)

include(backend/CMakeLists.txt)
add_executable(${PROJECT_NAME} ${BACKEND})

target_sources(imgui
    PRIVATE
        ${IMGUI_DIR}/imgui_demo.cpp
        ${IMGUI_DIR}/imgui_draw.cpp
        ${IMGUI_DIR}/imgui_tables.cpp
        ${IMGUI_DIR}/imgui_widgets.cpp
        ${IMGUI_DIR}/imgui.cpp
    PUBLIC
        ${BACKEND}
)

target_include_directories( 
    imgui
    PUBLIC ${IMGUI_DIR}
    PUBLIC ${IMGUI_DIR}/backends
)