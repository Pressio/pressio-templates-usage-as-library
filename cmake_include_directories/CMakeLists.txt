cmake_minimum_required(VERSION 3.18.0)
set(example pressio-example)
project(${example})

include_directories(${${example}_SOURCE_DIR}/../../include)

add_executable(${example} ${CMAKE_CURRENT_SOURCE_DIR}/../main.cpp)
target_compile_definitions(${example} PUBLIC PRESSIO_ENABLE_TPL_EIGEN)
