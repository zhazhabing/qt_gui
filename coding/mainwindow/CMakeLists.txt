
cmake_minimum_required (VERSION 2.8)

project(mainwindow)

# Find includes in corresponding build directories
set(CMAKE_INCLUDE_CURRENT_DIR ON)
# Instruct CMake to run moc automatically when needed
set(CMAKE_AUTOMOC ON)
# Create code from a list of Qt designer ui files
set(CMAKE_AUTOUIC ON)

# Find the QtWidgets library
find_package(Qt4 REQUIRED)

# Populate a CMake variable with the sources
set(mainwindow_SRCS
    main.cpp
)

# Tell CMake to create the mainwindow executable
add_executable(mainwindow WIN32 ${mainwindow_SRCS})

# Use the Widgets module from Qt 4.
target_link_libraries(mainwindow ${QT_LIBRARIES})