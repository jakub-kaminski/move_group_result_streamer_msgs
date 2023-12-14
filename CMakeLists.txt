cmake_minimum_required(VERSION 3.5)
project(move_group_result_streamer_msgs)

# Default to C++14
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(sensor_msgs REQUIRED)
find_package(std_msgs REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/JointStateArray.msg"
  DEPENDENCIES sensor_msgs std_msgs
)

ament_package()
