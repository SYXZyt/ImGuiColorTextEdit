cmake_minimum_required(VERSION 3.26)

project(ImGuiTextEdit)

include_directories(${CMAKE_SOURCE_DIR}/library/ImGui)
include_directories(${CMAKE_CURRENT_LIST_DIR}/include)

add_library(ImGuiTextEdit STATIC TextEditor.cpp include/ImGuiTextEdit/TextEditor.h)

target_link_libraries(ImGuiTextEdit imgui)