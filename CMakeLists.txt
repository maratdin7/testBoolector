set(CMAKE_C_STANDARD 99)
cmake_minimum_required(VERSION 3.5.1)
set(PROJECT_NAME testBoolector C)
project(${PROJECT_NAME})

set(BOOLECTOR_DIR /home/maratdin7/boolector/)
set(BOOLECTOR_INCLUDE_DIRS ${BOOLECTOR_DIR}/src)
set(BOOLECTOR_INCLUDE_LIB ${BOOLECTOR_DIR}/build/lib)
include_directories(${BOOLECTOR_INCLUDE_DIRS})
link_directories(${BOOLECTOR_INCLUDE_LIB}/libboolector.a )

add_executable(testBoolector main.c)
target_link_libraries(testBoolector ${BOOLECTOR_INCLUDE_LIB}/libboolector.a)