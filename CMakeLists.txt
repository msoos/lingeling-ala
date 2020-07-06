cmake_minimum_required(VERSION 3.3 FATAL_ERROR)
project(lingeling-ala)

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package (Threads REQUIRED)

add_definitions(-DNCHKSOL)
add_definitions(-DNLGLPICOSAT)


add_executable(lingeling
    lglbnr.c
    lglib.c
    lglmain.c
)
target_link_libraries(lingeling
    LINK_PUBLIC ${CMAKE_THREAD_LIBS_INIT}
    m
)

