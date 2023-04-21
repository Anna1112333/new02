cmake_minimum_required(VERSION 3.14)

project(Task_02_1 LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS Core)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Core Network Sql)

add_executable(Task_02_1
  main.cpp
)
target_link_libraries(Task_02_1 Qt${QT_VERSION_MAJOR}::Core Qt6::Network Qt6::Sql)

install(TARGETS Task_02_1
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
