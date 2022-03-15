cmake_minimum_required(VERSION 3.0.2)
project(rosbot_teleop)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  roscpp
  rospy
)

catkin_package(CATKIN_DEPENDS)

include_directories(${catkin_INCLUDE_DIRS})

add_executable(teleop src/teleop.cpp)
target_link_libraries(teleop ${catkin_LIBRARIES})