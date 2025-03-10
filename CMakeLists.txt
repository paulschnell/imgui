cmake_minimum_required(VERSION 3.13)

project(imgui
    VERSION 1.90.5
    DESCRIPTION "Dear ImGui: Bloat-free Graphical User interface for C++ with minimal dependencies "
    LANGUAGES C CXX
)

set(CMAKE_C_STANDARD 17)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

file(GLOB SOURCE_FILES "*.h" "*.cpp" ${IMGUI_ADDITIONAL_SOURCE_FILES})

add_library(imgui ${SOURCE_FILES})

target_include_directories(imgui PUBLIC . ${IMGUI_ADDITIONAL_INCLUDE_DIRS})
