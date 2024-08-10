cmake_minimum_required(VERSION 3.10)
project(gbit LANGUAGES CXX)

# Source files for gbit lib
set(GBIT_SOURCES
    ${CMAKE_CURRENT_SOURCE_DIR}/disassembler.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/inputstate.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/ref_cpu.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/tester.cpp
)

# Create lib from gbit
add_library(${PROJECT_NAME} ${GBIT_SOURCES})

# Add external lib include
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})