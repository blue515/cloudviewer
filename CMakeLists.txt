cmake_minmum_required(VERSION 2.8 FATAL_ERROR)
project(cloudviewer)

find_package(PCL 1.2 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable(cloudviewer cloudviewer.cpp)
target_link_libraries (cloudviewer ${PCL_LIBRARIES})
