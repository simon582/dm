cmake_minimum_required(VERSION 2.8.4)
project(bdl_lib)
ADD_SUBDIRECTORY(src bin)
ADD_SUBDIRECTORY(util)
ADD_SUBDIRECTORY(ts)
ADD_SUBDIRECTORY(dm)

set(CMAKE_C_FLAGS "-std=c99 -O3 -pipe -Wall -Wextra")

INSTALL(FILES COPYRIGHT README DESTINATION share/doc)
INSTALL(DIRECTORY data/ DESTINATION data PATTERN "*svn*" EXCLUDE)
INSTALL(DIRECTORY doc/ DESTINATION share/doc PATTERN "*svn*" EXCLUDE)

