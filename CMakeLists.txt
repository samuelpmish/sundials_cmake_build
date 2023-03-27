cmake_minimum_required(VERSION 3.16)
project(myproject LANGUAGES CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS 1)

set(CMAKE_CXX_STANDARD 17)

include(FetchContent)
include(ExternalProject)
include(cmake/options.cmake)
include(cmake/sundials.cmake)

add_executable(cvodes_ex src/cvodes_example.cpp)
target_link_libraries(cvodes_ex PUBLIC sundials_cvodes)

add_executable(kinsol_ex src/kinsol_example.cpp)
target_link_libraries(kinsol_ex PUBLIC sundials_kinsol)
