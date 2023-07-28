cmake_minimum_required(VERSION 3.26...3.26)

# Project name and a few useful settings. Other commands can pick up the results
project("ImGui_Piano"
	VERSION 1.1.0
	DESCRIPTION "Piano keyboard for ImGui"
	LANGUAGES CXX
)

find_package(imgui REQUIRED)

#Generate the static library from the library sources
message(STATUS "Building imgui_piano Library...")
add_library(imgui_piano STATIC "src/imgui_piano.cpp")
target_link_libraries(imgui-imgui_piano PRIVATE imgui)
target_include_directories(imgui_piano PUBLIC "${PROJECT_SOURCE_DIR}/include")
