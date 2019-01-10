cmake_minimum_required (VERSION 2.8)

project(mainwindow)

# Find the QtWidgets library
find_package(Qt4 REQUIRED)

# Find includes in corresponding build directories
set (in ${PROJECT_SOURCE_DIR})
include_directories (${in})

add_subdirectory (mainwindow)

INCLUDE(${QT_USE_FILE})
ADD_DEFINITIONS(${QT_DEFINITIONS})