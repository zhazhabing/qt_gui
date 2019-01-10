cmake_minimum_required (VERSION 2.8)

project(mainwindow)

find_package(Qt4 REQUIRED)

set (in ${PROJECT_SOURCE_DIR})
include_directories (${in})

set(project_SOURCES 
	main.cpp)

INCLUDE(${QT_USE_FILE})
ADD_DEFINITIONS(${QT_DEFINITIONS})

ADD_EXECUTABLE(
	mainwindow ${project_SOURCES}
)

TARGET_LINK_LIBRARIES(mainwindow ${QT_LIBRARIES})