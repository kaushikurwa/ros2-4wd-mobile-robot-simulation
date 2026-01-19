# ROS2 4WD Mobile Robot Simulation (Gazebo & RViz)

## Overview

A ROS2 4-Wheel-Drive Mobile Robot Simulated in Gazebo and visualized in RViz.  
This robot integrates LiDAR and RGB camera sensors and supports teleoperation, providing a complete baseline for mobile robot perception, motion, and system bringup.

The project focuses on:
- **ROS 2 modular architecture** using separate description and bringup packages
- **Sensor integration** with LiDAR and camera plugins
- **Differential drive kinematics** for realistic motion
- **Simulation-first validation** using Gazebo and RViz

---
## System Requirements

- Ubuntu 22.04
- ROS 2 Humble
- Gazebo 11
- Python 3.10+

---
## Features

- **4WD Differential Drive Robot:** Realistic wheel-based motion model  
- **LiDAR Sensor Integration:** Publishes `/laser_scan` data for perception and mapping  
- **RGB Camera Sensor:** Streams image data for vision-based tasks  
- **Gazebo Simulation:** Physics-based environment for testing robot behavior  
- **RViz Visualization:** TF tree, robot model, laser scan, and sensor data  
- **Keyboard Teleoperation:** Manual control using velocity commands  

---

## System Architecture

1. **Robot Description:**  
   URDF/Xacro files define the robot structure, wheels, sensors, and frames.

2. **Simulation Bringup:**  
   Gazebo world, controllers, and plugins are launched through ROS2 launch files.

3. **Sensor Data Flow:**  
   LiDAR and camera plugins publish sensor topics in real time.

4. **Visualization & Control:**  
   RViz displays TF, LaserScan, and robot state while teleop sends `/cmd_vel`.

---

## Repository Structure

```
4wd_ws/
├── src/
│ ├── my_robot_description          # URDF, Xacro, RViz configs
│ └── my_robot_bringup              # Gazebo world, controllers, launch files
├── screenshots/
└── README.md
```
---

## Visuals

<p align="center">
  <img src="screenshots/Screenshot from 2026-01-19 20-25-14.png" width="500">
</p>

<p align="center">
  <img src="screenshots/Screenshot from 2026-01-19 20-25-30.png" width="500">
</p>

<p align="center">
  <img src="screenshots/Screenshot from 2026-01-19 20-27-47.png" width="500">
</p>

---

## How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/kaushikurwa/ros2-4wd-mobile-robot-simulation.git

## Dependencies

### Core Dependencies
## Building the Project

```bash
cd ~ 4wd_ws/
colcon build
source install/setup.bash
```
## Configuration

### Lidar Parameters

Edit `src/my_robot_description/urdf/lidar_sensor.xacro` to modify:
- Scan range (min/max)
- Update rate
- Sample count
- Visualization settings

## Future Work

- Integrate Nav2 for autonomous navigation
- Add SLAM (RTAB-Map / SLAM Toolbox)
- Implement waypoint-based navigation
- Extend simulation to real hardware deployment


## Contributing

Contributions are welcome! Please feel free to submit issues and pull requests.

## Author

kaushikurwa

## Acknowledgments

- ROS 2 community
- Gazebo simulation platform

