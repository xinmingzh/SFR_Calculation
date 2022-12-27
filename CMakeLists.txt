cmake_minimum_required(VERSION 3.22)
project(SFR_Calculation)

set(CMAKE_CXX_STANDARD 14)

include_directories(src)

find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable(SFR_Calculation
        src/main.cpp
        src/sfr.cpp
        src/sfr.h)

target_link_libraries( SFR_Calculation ${OpenCV_LIBS} )
