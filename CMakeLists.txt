cmake_minimum_required(VERSION 3.19)

project("sdb" LANGUAGES CXX)

find_package(PkgConfig REQUIRED)
pkg_check_modules(readline REQUIRED IMPORTED_TARGET readline)

include(CTest)

add_subdirectory("src")
add_subdirectory("tools")

if (BUILD_TESTING)
    add_subdirectory("test")
endif()

set(CMAKE_TOOLCHAIN_FILE "C:/path/to/vcpkg/scripts/buildsystems/vcpkg.cmake" CACHE STRING "")

enable_testing()