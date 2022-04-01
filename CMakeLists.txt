cmake_minimum_required(VERSION 3.12)

project(MyProject VERSION 1.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(
    sayHello
    src/hello.h
    src/hello.cpp)

add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE sayHello)
target_compile_features(${PROJECT_NAME} PUBLIC cxx_std_20)

