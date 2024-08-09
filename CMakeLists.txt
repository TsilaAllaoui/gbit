cmake_minimum_required(VERSION 3.10)
project(gbit LANGUAGES CXX)

# Source files for gbit lib
file(GLOB_RECURSE GBIT_SOURCES "/*.cpp")

# Create lib from gbit
add_library(${PROJECT_NAME} ${GBIT_SOURCES})

# Add external lib include
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/)