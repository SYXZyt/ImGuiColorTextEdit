cmake_minimum_required(VERSION 3.26)

project(ImGuiTextEdit)

if (NOT DEFINED SAGE_DIR)
    message(FATAL_ERROR "SAGE_DIR has not been set!")
endif()

include_directories(${SAGE_DIR}/library/ImGui)
include_directories(${CMAKE_CURRENT_LIST_DIR}/include)

add_library(ImGuiTextEdit STATIC TextEditor.cpp include/ImGuiTextEdit/TextEditor.h)

target_link_libraries(ImGuiTextEdit imgui)