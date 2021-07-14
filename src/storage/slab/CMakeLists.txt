set(SOURCE
    hashtable.c
    item.c
    slab.c
    MyWrapper.cc)

set(CMAKE_CPP_COMPILER "g++-4.2")
set(CMAKE_CPP_FLAGS "${CMAKE_CPP_FLAGS} -std=c++11 -Wall -fprofile-arcs -ftest-coverage")

add_library(slab ${SOURCE})
target_link_libraries(slab datapool)
