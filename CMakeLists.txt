cmake_minimum_required(VERSION 3.5)
project(hello)

set(CMAKE_C_STANDARD 11)

# python stuff
find_package(PythonLibs REQUIRED)
include_directories(${PYTHON_INCLUDE_DIRS})

set(SOURCE_FILES src/hello.c)
add_library(hello SHARED ${SOURCE_FILES})
set_target_properties(hello PROPERTIES PREFIX "")
target_link_libraries(hello ${PYTHON_LIBRARIES})
