cmake_minimum_required(VERSION 3.20)
set(CMAKE_OSX_DEPLOYMENT_TARGET 10.15 CACHE STRING "MIN OSX" FORCE)

project(AV_STREAM_CPP VERSION 0.1)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_library(COCOA_LIBRARY Cocoa)

include_directories(include)
add_library(AV_STREAM_CPP SHARED
            src/AVFoundationWrapper.mm
            src/main.cpp
        )