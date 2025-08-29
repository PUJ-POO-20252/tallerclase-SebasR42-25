cmake_minimum_required(VERSION 4.0)
project(GradesAnalyze)

set(CMAKE_CXX_STANDARD 20)

add_executable(GradesAnalyze main.cpp
        calificaciones_utils.cpp
        calificaciones_utils.h)
