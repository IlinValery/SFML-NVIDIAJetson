cmake_minimum_required(VERSION 3.5)

set(PROJECT_NAME test_sfml_cpp1)
project(${PROJECT_NAME})

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES programm.cpp)

set(SFML_DIR "${PROJECT_SOURCE_DIR}/SFML-2.5.1")
set(SFML_ROOT ${SFML_DIR})
set(CMAKE_MODULE_PATH "${SFML_DIR}/cmake/Modules" ${CMAKE_MODULE_PATH})
find_package(SFML 2 COMPONENTS system window graphics audio network REQUIRED)

include_directories(${SFML_INCLUDE_DIR})
add_executable(${PROJECT_NAME} ${SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} ${SFML_LIBRARIES})
