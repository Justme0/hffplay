aux_source_directory(. DIR_LIB_SRCS)
include_directories(${PROJET_SOURCE_DIR}/libavutil)
add_library (avcodec ${DIR_LIB_SRCS})
