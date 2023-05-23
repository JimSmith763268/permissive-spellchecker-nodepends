cmake_minimum_required(VERSION 3.14)

project(permissive-spellchecker-nodepends LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(permissive-spellchecker-nodepends SHARED
  permissive-spellchecker_global.h
  permissivespellchecker.cpp
  permissivespellchecker.h
)

target_compile_definitions(permissive-spellchecker-nodepends PRIVATE PERMISSIVESPELLCHECKER_LIBRARY)
