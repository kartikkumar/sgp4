cmake_minimum_required(VERSION 2.8.6)

project(sgp4)
add_subdirectory(cpp)

# Build option: specify if shared libraries should be built. Default is set to OFF, meaning that
# static libraries will be built unless specified otherwise.
OPTION(BUILD_SHARED_LIBS "Build shared libraries" OFF)