cmake_minimum_required(VERSION 3.18)
project(ocle)

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCL REQUIRED)
include_directories(${OpenCL_INCLUDE_DIRS})
link_directories(${OpenCL_LIBRARY})

add_executable(ocle test.cpp src/ocle.cpp src/Base.cpp src/AES.cpp)
target_link_libraries (ocle ${OpenCL_LIBRARY})
