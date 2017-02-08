cmake_minimum_required(VERSION 2.8.3)
project(riptide_bringup)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

add_executable(hello src/hello.cpp)
add_dependencies(hello riptide_msgs_gencpp)
target_link_libraries(hello ${catkin_LIBRARIES})

include_directories(${catkin_INCLUDE_DIRS})

