project(https_client)
cmake_minimum_required(VERSION 3.2)

add_definitions("-std=c++11")

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_executable(https_client https_client.cpp)
target_link_libraries(https_client ${CONAN_LIBS} pthread ssl crypto)

