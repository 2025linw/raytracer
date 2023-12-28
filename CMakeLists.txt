# Set minimum required version of cmake
cmake_minimum_required(VERSION 3.10)

# Create project
project(raytracer)

# Set CXX standard
set(CMAKE_CXX_STANDARD 17)

# Make list of all source files
set(
    SOURCES
    src/main.cpp
)

# Make a list of all directories to look in for includes
set(
    INCLUDE_DIRS
    include
)

# List of all libraries
set(
    LIBS
)

# Define what is being produced (an executable)
add_executable(${PROJECT_NAME} ${SOURCES} ${INCLUDES})

# What directories to look for when including a file; `-I` in g++
include_directories(${INCLUDE_DIRS})

# What libraries to link to; `-l` in g++
target_link_libraries(${PROJECT_NAME} PRIVATE ${LIBS})
