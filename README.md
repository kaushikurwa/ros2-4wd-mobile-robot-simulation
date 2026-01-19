# ROS2 4WD Mobile Robot

A ROS2-based 4WD mobile robot simulated in Gazebo and visualized in RViz.
Includes LiDAR and RGB camera sensor integration.

## Packages
- my_robot_description
- my_robot_bringup

## Run
colcon build
source install/setup.bash
ros2 launch my_robot_bringup gazebo.launch.py
