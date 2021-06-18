cmake_minimum_required(VERSION 3.5)

project(hipSYCL_hello_world)

find_package(hipSYCL CONFIG REQUIRED)

set(SOURCES
  src/main.cpp
)

add_executable(${PROJECT_NAME}
  ${SOURCES}
)

add_sycl_to_target(
  TARGET ${PROJECT_NAME}
  SOURCES ${SOURCES}
)
