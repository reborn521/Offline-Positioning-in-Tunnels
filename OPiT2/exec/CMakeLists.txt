#check for the mininum version of cmake
cmake_minimum_required (VERSION 3.0 FATAL_ERROR)

#add library dependancies
add_subdirectory (./../shared shared)

#include_directories
include_directories (${SHARED_INCLUDE_DIR})

#main source
set (EXEC_SOURCE Main.cpp)
add_executable (OPiT2 ${EXEC_SOURCE})
target_link_libraries (OPiT2 shared ${OpenCV_LIBS} ${PCL_LIBRARIES})
