# arm_gazebo Dockerfile

This repository provides a corrected `Dockerfile` and `patches/` directory for the `arm_gazebo` Docker image, based on the original project at [https://github.com/iocchi/arm_gazebo](https://github.com/iocchi/arm_gazebo). The `Dockerfile` resolves dependency issues by building `eigenpy`, `hpp-fcl`, and `pinocchio` from source and includes necessary patches.

## Purpose
This `Dockerfile` ensures a working ROS Noetic environment for the `arm_gazebo` project, fixing dependencies for `libfranka`, `franka_ros`, Universal Robots, and Robotiq gripper packages.

## System Requirements
- **OS**: Ubuntu 20.04 (tested)
- **Docker**: Version 26.1.3 (or 19.03+)
- **Hardware**: 8GB+ RAM, 4+ CPU cores, 10GB+ disk space

## Usage
1. Clone the original `arm_gazebo` repository:
   ```bash
   git clone https://github.com/iocchi/arm_gazebo.git
   cd arm_gazebo/docker
   ```
2. Download this repository’s `Dockerfile` and `patches/` directory:
   ```bash
   git clone https://github.com/victorrobocup/arm_gazebo.git victor_docker
   cp victor_docker/Dockerfile .
   cp -r victor_docker/patches .
   ```
3. Follow the build instructions in the original `arm_gazebo` repository.

## Notes
- The build may take significant time due to compiling dependencies.
- Ensure a stable internet connection for cloning repositories.
- The `patches/` directory must be in `arm_gazebo/docker` alongside the `Dockerfile`.

## Original Project
Refer to [https://github.com/iocchi/arm_gazebo](https://github.com/iocchi/arm_gazebo) for the original `arm_gazebo` project, including build instructions and license.
