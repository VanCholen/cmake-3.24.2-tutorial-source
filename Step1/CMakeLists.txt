cmake_minimum_required(VERSION 3.10)

# set the project name
project(Tutorial VERSION 3.6.1)

# pre-defined variables 
message(${Tutorial_VERSION})
message(${Tutorial_VERSION_MAJOR})
message(${Tutorial_VERSION_MINOR})
message(${Tutorial_VERSION_PATCH})


# set standard c++ 11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# add the executable
add_executable(Tutorial tutorial.cxx)
configure_file(TutorialConfig.h.in TutorialConfig.h)
target_include_directories(Tutorial PUBLIC
                           "${PROJECT_BINARY_DIR}"
)
