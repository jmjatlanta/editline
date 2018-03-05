cmake_minimum_required(VERSION 2.8.9)

project(editline)

include_directories(include)

add_definitions(-DHAVE_MALLOC_H)
add_definitions(-DHAVE_STRING_H)
add_definitions(-DHAVE_STDLIB_H)
add_definitions(-DHAVE_DIRENT_H)
add_definitions(-DHAVE_SIGNAL_H)
add_definitions(-DHAVE_SGTTY_H)
add_definitions(-DHAVE_TERMIO_H)
add_definitions(-DSYS_UNIX)
add_definitions(-DHAVE_TCGETATTR)

set (SOURCES src/editline.c src/complete.c src/sysunix.c)

add_library(editline STATIC ${SOURCES})
