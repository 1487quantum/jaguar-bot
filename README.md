# jaguar-bot
This repository contains the codes & drivers used for the autonomous mobile robot project (FYP) to perform autonomous navigation. The *conifer-dashboard* (web dashboard) is used to display the telemetry and relevant information of the robot via a local web server with *NodeJS*. (The repo is located over here: https://github.com/1487quantum/conifer-dashboard)

## System
- Ubuntu 14.04 LTS (64-bit)
- ROS Indigo

## ROS Packages
### System
The following ROS packages are required to be installed system wide: 
- Gmapping: ros-indigo-gmapping
- Map server: ros-indigo-map_server
- AMCL: ros-indigo-amcl
- Move base: ros-indigo-move-base
- Camera Info Manager (Py): ros-indigo-camera-info-manage-py

To do so, simply run the following command, replacing *package_name* with the ones you need.
```
$ sudo apt-get install ros-indigo-[package_name]
```

### Local
All the packages in this repo should be cloned & place into your workspace.
```
$ git clone https://github.com/1487quantum/jaguar-bot.git
```

## Directories
An overview of the purpose of the various directories:
- *joy*: Joystick driver
- *teleop_twist_joy*: Process /joy -> /cmd_vel
- *diff_drive_controller*: Process /cmd_vel -> /joint_trajectory
- *kangaroo_x2_driver*: Process /joint_trajectory -> /joint_state, controls the motor
- *lms1xx_driver*: Lidar Driver (LMS111)
- *robot_core*: Main control launch/config files to run the robot is here
- *axis_camera*: Axis Web camera

