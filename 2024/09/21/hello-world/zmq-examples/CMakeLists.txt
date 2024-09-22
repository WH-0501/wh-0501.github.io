---
title: ZeroMQ CMakeLists.txt
date: 2024-09-07 20:37:29
tags: 
    - ZeroMQ
categories:
    - 数据通信
    - ZeroMQ

---



```cmake
cmake_minimum_required(VERSION 2.8)
project(zmq-examples)

include_directories(${PROJECT_SOURCE_DIR}/include)

add_executable(hello src/hello.c)
target_link_libraries(hello czmq zmq sodium)

add_executable(multithreaded_server src/multithreaded_server.c)
target_link_libraries(multithreaded_server czmq zmq sodium pthread)

add_executable(multithreaded_relay src/multithreaded_relay.c)
target_link_libraries(multithreaded_relay czmq zmq sodium pthread)

add_executable(syncpub src/syncpub.c)
target_link_libraries(syncpub czmq zmq sodium)
add_executable(syncsub src/syncsub.c)
target_link_libraries(syncsub czmq zmq sodium)
```

