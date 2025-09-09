cmake_minimum_required(VERSION 4.1.1)
project(demo02 VERSION 1.0 LANGUAGES CXX)
set((CMAKE_CXX_FLAGS "{CMAKE_CXX_FLAGS} --Wall"))

SET(CMAKE_BUILD_TYPE Debug)

include_directories(${CMAKE_SOURCE_DIR}/Inc)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)
aux_source_directory(${CMAKE_SOURCE_DIR}/Src SRC_LIST)
add_executable(
    myTest_EXE
    ${SRC_LIST}
)