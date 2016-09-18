
cmake_minimum_required (VERSION 2.8)
# project information
project (hffplay)

aux_source_directory(. DIR_SRCS)

include_directories(${PROJET_SOURCE_DIR}/libavutil)
include_directories(/usr/include/SDL)

# add sub directories
add_subdirectory(libavformat)
add_subdirectory(libavcodec)

add_executable(hffplay ffplay.c)

#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++0x")
# Add dependent libraries
target_link_libraries(hffplay /usr/lib/x86_64-linux-gnu/libSDL.so avformat avcodec)
