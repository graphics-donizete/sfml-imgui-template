cmake_minimum_required(VERSION 3.10.0)
project(sfml-imgui-template VERSION 0.1.0 LANGUAGES C CXX)

add_subdirectory(${CMAKE_SOURCE_DIR}/third_party/SFML)

add_executable(
    sfml-imgui-template
    main.cpp)

target_link_libraries(
    sfml-imgui-template
    SFML::Window)

