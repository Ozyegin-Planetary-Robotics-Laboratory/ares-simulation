cmake_minimum_required(VERSION 3.0.2)
project(ares_rover)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  gazebo_ros
)

catkin_package(
  CATKIN_DEPENDS roscpp rospy std_msgs gazebo_ros
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
