cmake_minimum_required(VERSION 3.20)
set(CMAKE_OSX_DEPLOYMENT_TARGET 10.15 CACHE STRING "MIN OSX" FORCE)

project(
    AV_STREAM_CPP 
    VERSION 0.1
)

# set(CMAKE_CXX_STANDARD 20)
# set(CMAKE_CXX_STANDARD_REQUIRED True)

find_library(COCOA_LIBRARY Cocoa)
find_library(AVFOUNDATION_LIBRARY AVFoundation)

include_directories(include)

# add_library(avStreamLib STATIC
#             src/AVFoundationWrapper.mm
#             include/AVFoundationWrapper.h)

add_executable(avStream src/main.cpp src/AVFoundationWrapper.mm) #This is a teste executable which loads our static lib
#target_link_libraries(avStream PRIVATE avStreamLib)