cmake_minimum_required(VERSION 3.5)
project(sparrow)
set(CMAKE_CXX_STANDARD 11)

# Set architecture
# set(CMAKE_OSX_ARCHITECTURES x86_64 arm64)
set(CMAKE_OSX_ARCHITECTURES "x86_64")
# set(CMAKE_OSX_ARCHITECTURES "arm64")


add_subdirectory(sparrow/_lib/src/LinearModel)
add_subdirectory(sparrow/_lib/src/OtherModule)