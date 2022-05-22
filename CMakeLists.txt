cmake_minimum_required(VERSION 3.0.0)
project(tinyOS VERSION 0.1.0)

include_directories(include)

# add_executable(oc src/pc.c)
add_executable(tinyOS src/fish.c) 

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)
target_link_libraries(tinyOS PRIVATE Threads::Threads)
