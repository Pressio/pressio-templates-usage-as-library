cmake_minimum_required(VERSION 3.18.0)
set(example pressio-example)
project(${example})

set(PRESSIO_SOURCE_DIR ${${example}_SOURCE_DIR}/../..)
set(PRESSIO_OPS_INCLUDES ${PRESSIO_SOURCE_DIR}/pressio-ops/include)
set(PRESSIO_INCLUDES ${PRESSIO_SOURCE_DIR}/include)

include_directories(${PRESSIO_OPS_INCLUDES})
include_directories(${PRESSIO_INCLUDES})

add_executable(${example} ${CMAKE_CURRENT_SOURCE_DIR}/../main.cpp)
target_compile_definitions(${example} PUBLIC PRESSIO_ENABLE_TPL_EIGEN)
