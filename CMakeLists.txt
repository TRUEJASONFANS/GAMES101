cmake_minimum_required(VERSION 3.12)

set(CMAKE_CXX_STANDARD 17)

project(GAMES101)
#ucm_set_runtime(STATIC)
set(CMAKE_INSTALL_PREFIX ${CMAKE_HOME_DIRECTORY})



set(OpenCV_DIR ${CMAKE_HOME_DIRECTORY}/opencv/build)
set(Eigen3_DIR ${CMAKE_HOME_DIRECTORY}/eigen)

find_package( OpenCV REQUIRED )
find_package( Eigen3 REQUIRED)

add_subdirectory(00)
add_subdirectory(01)
add_subdirectory(02)
add_subdirectory(03)
add_subdirectory(04)
add_subdirectory(05)
add_subdirectory(06)
add_subdirectory(07)



install(TARGETS 00 01 02 03 04 05 06 07 DESTINATION  output)
install(DIRECTORY 03/models DESTINATION output)
install(DIRECTORY 06/models DESTINATION output)
install(DIRECTORY 07/models DESTINATION output)