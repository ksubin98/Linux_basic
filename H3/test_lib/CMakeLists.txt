cmake_minimum_required(VERSION 3.0.2)
project(LinuxProg)
find_package(Threads)
set(CMake_BUILD_TYPE Release)

include_directories(/user/lib)
file(GLOB_RECURSE SOURCES "./*.cpp")

add_library(LinuxProg SHARED ${SOURCES})
target_link_libraries(LinuxProg ${CMAKE_THREAD_LIBS_INIT})
install(TARGETS LinuxProg DESTINATION /user/lib)
