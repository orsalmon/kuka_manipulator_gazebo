KUKA KR5 manipulator gazebo
===========================
This is a little project in ROS & Gazebo of 3DoF KUKA robotic arm.

The manipulator gets [x y z] cordinates, duration, and calculating linaer trajectory with trapezoidal velocity profile.

Prerequisites:
==============
Install git:
------------
sudo apt-get install ros-indigo-move-base

sudo apt-get install ros-indigo-ros-control ros-indigo-ros-controllers

sudo apt-get install ros-indigo-gazebo-ros-control

Install this package in your catkin_ws
--------------------------------------
(in a new terminal window) "source ~/catkin_ws/devel/setup.bash"

"cd ~/catkin_ws/src"

"git clone https://github.com/orsalmon/KUKA_KR5_manipulator_gazebo.git"

"cd .."

"catkin_make"

Launching The Manipulator In GAZEBO Simulator:
==============================================
(in a new terminal window)

"source ~/catkin_ws/devel/setup.bash"

"roslaunch manipulator_gazebo manipulator_empty_world.launch"

(in a new terminal window)

"source ~/catkin_ws/devel/setup.bash"

"rosrun manipulator_gazebo move_arm_server"

To send a command:
------------------
(in a new terminal window)

"source ~/catkin_ws/devel/setup.bash"

"rosservice call /move_arm"

now press "TAB" for auto complete and refill the desired values.

