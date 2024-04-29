cmake_minimum_required(VERSION 3.2)

project(gRPC-example)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++20 -O3")
include(FetchContent)
# find_package()
FetchContent_Declare(
    gRPC
  GIT_REPOSITORY https://github.com/grpc/grpc
  GIT_TAG        v1.63.0
)
set(FETCHCONTENT_QUIET OFF)
FetchContent_MakeAvailable(gRPC)

add_executable(my_exe my_exe.cpp)
target_link_libraries(my_exe grpc++)



