cmake_minimum_required(VERSION 2.8.3)
project(robotiq_control)

find_package(catkin REQUIRED COMPONENTS 
  rospy
  dynamic_reconfigure
)

catkin_python_setup()

generate_dynamic_reconfigure_options(
  cfg/GripperConfig.cfg
)

catkin_package(
  CATKIN_DEPENDS rospy dynamic_reconfigure
)
