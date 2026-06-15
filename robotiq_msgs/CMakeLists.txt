cmake_minimum_required(VERSION 3.8)
project(robotiq_msgs)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)

# The .msg/.action contain only primitive fields, so no interface DEPENDENCIES are
# needed. action_msgs is pulled in automatically for the action's goal-status plumbing.
rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/CModelCommand.msg"
  "msg/CModelStatus.msg"
  "action/CModelCommand.action"
)

ament_package()
