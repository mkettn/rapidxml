cmake_minimum_required(VERSION 3.12)
project("rapidxml" VERSION 1.13
  DESCRIPTION "Header-only library for C++11 to parse (read) XML data"
  HOMEPAGE_URL "https://github.com/mkettn/rapidxml")

add_library(${PROJECT_NAME} INTERFACE IMPORTED)
add_library(${PROJECT_NAME}::${PROJECT_NAME} ALIAS ${PROJECT_NAME})

target_include_directories(rapidxml SYSTEM INTERFACE
  ${CMAKE_CURRENT_SOURCE_DIR}/include
)

