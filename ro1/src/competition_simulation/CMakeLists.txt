cmake_minimum_required(VERSION 2.8.3)
project(competition_simulation)#自定义ros包的名字

#依赖包配置
find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  message_generation
  tf
)

#消息生成配置
generate_messages(
  DEPENDENCIES
  std_msgs
)
 #包导出配置
catkin_package(
  CATKIN_DEPENDS message_runtime
)

#包含目录配置
include_directories(
    include
    ${catkin_INCLUDE_DIRS}
)