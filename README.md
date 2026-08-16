# ROS 2 & Gazebo Simulation Framework for Mobile Rover

A custom 4-wheeled differential drive rover simulated using **ROS 2 (Jazzy)** and **Gazebo Sim 8 (Harmonic)**. Features custom URDF robot modeling, physical link inertias, differential drive dynamics, and real-time ROS 2 state verification.

Key Features
Custom URDF Modeling Built base chassis, 4 continuous wheel joints, and top-mounted 2D LiDAR frame with accurate inertial and visual properties.
* **Gazebo Sim Integration**: Configured `gz-sim-diff-drive-system` and `gz-sim-sensors-system` plugins for realistic physics and sensor emulation.
* **ROS 2 Bridge**: Bi-directional node communication via `ros_gz_bridge` handling `/cmd_vel` command velocity inputs and `/odom` telemetry output.
* **Telemetry Verification**: Validated state estimation and kinematic loops using ROS 2 CLI utilities (`ros2 topic`, `check_urdf`).

##  Tech Stack
* **OS**: Ubuntu 24.04 LTS (WSL2)
* **Framework**: ROS 2 Jazzy
* **Simulator**: Gazebo Sim 8 (Harmonic)
* **Languages**: XML / URDF, Python, Bash

##  How to Run

1. **Clone the repository:**
   ```bash
   mkdir -p ~/rover_ws/src
   cd ~/rover_ws/src
   git clone [https://github.com/bhosaleharsh24/ros2-rover-gazebo-simulation.git](https://github.com/bhosaleharsh24/ros2-rover-gazebo-simulation.git) rover_description
   cd ~/rover_ws
   colcon build
   source install/setup.bash
