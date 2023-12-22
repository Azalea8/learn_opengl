cmake_minimum_required(VERSION 3.27)
set(VCPKG_TARGET_TRIPLET "x64-mingw-dynamic" CACHE STRING "" FORCE)
project(01)

set(CMAKE_CXX_STANDARD 14)

add_executable(01 main.cpp)

find_package(glad CONFIG REQUIRED)
target_link_libraries(01 PRIVATE glad::glad)

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(01 PRIVATE glfw)
