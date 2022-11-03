cmake_minimum_required(VERSION 3.5)

project (hello_headers)

set(SOURCES
    src/Hello.cpp
    src/main.cpp
)#创建一个变量，名字叫SOURCE。它包含了所有的cpp文件。

add_executable(${PROJECT_NAME} ${SOURCES})

target_include_directories(${PROJECT_NAME}
    PRIVATE
        ${PROJECT_SOURCE_DIR}/include    
)#设置这个可执行文件hello_headers需要包含的库的路径


message(CMAKE_SOURCE_DIR : ${CMAKE_SOURCE_DIR})
message(CMAKE_CURRENT_SOURCE_DIR:${CMAKE_CURRENT_SOURCE_DIR})
message(PROJECT_SOURCE_DIR:${PROJECT_SOURCE_DIR})
message(CMAKE_BINARY_DIR:${CMAKE_BINARY_DIR})
message(CMAKE_CURRENT_BINARY_DIR:${CMAKE_CURRENT_BINARY_DIR})
message(PROJECT_BINARY_DIR:${PROJECT_BINARY_DIR})