# Define minimum version of CMake
cmake_minimum_required(VERSION 3.13.1)

# Set project name
project(my-motion)

# Set C/C++ standards
# set(CMAKE_CXX_FLAGS "-std=gnu++14")
# set(CMAKE_C_FLAGS "-std=gnu11")
# set(CMAKE_EXE_LINKER_FLAGS "-stdlib=libc++")
set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED TRUE)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

# Location of executable source file. Target must be named "app."
add_executable(app
    main.c
    )

# Force use of C++ compiler (so main in C or C++ can call C++ functions)
set_source_files_properties(main.c PROPERTIES LANGUAGE CXX)

# Location of impulse library
add_subdirectory(lib)