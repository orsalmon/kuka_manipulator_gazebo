cmake_minimum_required(VERSION 2.8.3)
project(manipulator_gazebo)


find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  gazebo_ros
  message_generation
)

## Generate services in the 'srv' folder
add_service_files(
  FILES
  MoveArm.srv
)

generate_messages(
   DEPENDENCIES
   std_msgs
)

catkin_package(
    DEPENDS 
    CATKIN_DEPENDS roscpp rospy std_msgs message_runtime 
    INCLUDE_DIRS 
    LIBRARIES 
)

include_directories(include ${catkin_INCLUDE_DIRS})

add_executable(move_arm_server src/move_arm_server.cpp)
target_link_libraries(move_arm_server ${catkin_LIBRARIES})
add_dependencies(move_arm_server beginner_tutorials_gencpp)
