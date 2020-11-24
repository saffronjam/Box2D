cmake_minimum_required(VERSION 3.1.0)
project(Box2D)

file(GLOB INCLUDES "include" "src")
file(GLOB_RECURSE SRC_FILES "src/*.cpp")

add_library(Box2D ${SRC_FILES})

target_include_directories(Box2D PRIVATE "${INCLUDES}")
set (Box2D_INCLUDES "${INCLUDES}" PARENT_SCOPE)