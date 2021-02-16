cmake_minimum_required(VERSION 3.0.2)
project(TestLibrary)

set(PROJECT_LINK_LIBS libLinuxProg.so)
link_directories(~/LinuxProg/library_test/lib_build)
include_directories(~/LinuxProg/library_test)

add_executable(libtest test.cpp)
target_link_libraries(libtest ${PROJECT_LINK_LIBS})

