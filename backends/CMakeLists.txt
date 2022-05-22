# Only OpenGL and GLFW for now
list(APPEND BACKEND
    ${CMAKE_CURRENT_LIST_DIR}/imgui_impl_opengl3_loader.h
    ${CMAKE_CURRENT_LIST_DIR}/imgui_impl_opengl3.h
    ${CMAKE_CURRENT_LIST_DIR}/imgui_impl_opengl3.cpp
    ${CMAKE_CURRENT_LIST_DIR}/imgui_impl_glfw.h
    ${CMAKE_CURRENT_LIST_DIR}/imgui_impl_glfw.cpp
)