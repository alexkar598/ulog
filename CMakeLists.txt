cmake_minimum_required(VERSION 4.0)
add_library(ulog)

target_sources(ulog
    PUBLIC
        FILE_SET HEADERS
        BASE_DIRS include
        FILES
            include/ulog/ulog.h
            include/ulog/macros.h

    PRIVATE
        FILE_SET private_headers
        TYPE HEADERS
        BASE_DIRS .
        FILES
            rzcobs.h
            linker_symbols.h

    PRIVATE
        ulog.c
        rzcobs.c
)

target_include_directories(ulog PUBLIC include)