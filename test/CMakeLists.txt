cmake_minimum_required(VERSION 3.2)
set(This test)
project(${This} C CXX)

set(CMAKE_C_STANDARD 99)
set(CMAKE_CXX_STANDARD 17)

include_directories (
  ../rotation-logger/include
)

set(Sources
  test.cc
)

add_executable(${This} ${Sources})

target_link_libraries(${This} PUBLIC
  gtest_main
  gmock_main  
  rotation-logger
)