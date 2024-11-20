cmake_minimum_required(VERSION 3.27)
project(Genetic_Prototype)
set(GENETIC_PROTOTYPE_VERSION 0.0.1)

# Set C++ standard
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Options
option(GENERIC_PROTOTYPE_BUILD_TESTS "Build test programs" OFF)

# Add Genetic Prototype
add_subdirectory(Genetic_Prototype)

# Add Test if Genetic Prototype is the project
if (GENERIC_PROTOTYPE_BUILD_TESTS OR
        PROJECT_NAME STREQUAL CMAKE_PROJECT_NAME)
    add_subdirectory(Tests)
endif ()