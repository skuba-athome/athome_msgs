cmake_minimum_required(VERSION 2.8.3)
project(athome_msgs)

find_package(catkin REQUIRED COMPONENTS
	roscpp
	rospy
	std_msgs
	geometry_msgs
	message_generation
)

add_message_files(
  FILES
  navigation_goal.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

###################################
## catkin specific configuration ##
###################################
catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES athome_msgs
   CATKIN_DEPENDS message_runtime
#  DEPENDS system_lib
)


