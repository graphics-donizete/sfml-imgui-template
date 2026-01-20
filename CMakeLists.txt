cmake_minimum_required(VERSION 3.10.0)
project(sfml-imgui-template VERSION 0.1.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(${CMAKE_SOURCE_DIR}/third_party/SFML)

set(IMGUI_SFML_FIND_SFML OFF)
set(IMGUI_DIR ${CMAKE_SOURCE_DIR}/third_party/imgui)
add_subdirectory(${CMAKE_SOURCE_DIR}/third_party/imgui-sfml)

add_executable(
    sfml-imgui-template
    main.cpp)

target_link_libraries(
    sfml-imgui-template
    SFML::Window
    ImGui-SFML::ImGui-SFML)

