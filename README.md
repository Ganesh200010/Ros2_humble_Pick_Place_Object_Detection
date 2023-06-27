<p align="left">

<img src="https://img.shields.io/badge/Ubuntu-22.04-orange.svg" alt="Ubuntu 22.04">
<img src="https://img.shields.io/badge/Python-3.x-blue.svg?logo=python&logoColor=white">

</p>

# Ros2_humble

ROS2 (Robot Operating System 2) is a flexible framework for developing robotic systems. It provides a set of tools, libraries, and conventions that aid in building robot applications. ROS2 is designed to be more scalable, distributed, and real-time capable compared to its predecessor, ROS.

<p align="left">
  
# 1.1 Pick & Place
Pick-and-place is a common robotic task where a robot arm picks up an object from one location and places it in another. The arm's movement can be controlled using inverse kinematics, which involves calculating the joint angles required to achieve a desired end-effector position


<img width="50%" src="https://github.com/Ganesh200010/Ros2_humble_Pick_Place_Object_Detection/assets/125490197/447fcb4f-bd8e-4d32-b8f6-7ee6f39b5172"/>
<img width="35%" src="https://github.com/Ganesh200010/Ros2_humble_Pick_Place_Object_Detection/assets/125490197/2a1bc3cf-2a11-4ec5-9e6a-193e454f1d26"/>

</p>


# 1.2 Object Detection

Object detection is the process of identifying and locating objects within an image or a point cloud. ROS2 provides several packages and libraries that can be used for object detection tasks

-	Ensure proper sensor calibration to achieve accurate object detection results.

# 2. Environment Setup
   
The project uses [ROS2 Humble](https://docs.ros.org/en/humble/index.html) running on [Ubuntu 22.04.2 LTS (Jammy Jellyfish)](https://releases.ubuntu.com/jammy/)

The following tools are used for simulation and motion planning:

- [Gazebo](https://gazebosim.org/home): A physics-based 3D simulator extensively used in the robotics world.
- [RViz](http://wiki.ros.org/rviz): A 3D visualizer for sensor data analysis and robot state visualization.


# ⚙️ Commands 2 Implement

    
## 
        
        G


## Working

- The ROS 2-based humble pick and place robot utilizes the ROS 2 framework for communication and coordination between its components.
- It employs object detection algorithms to identify objects in its environment, enabling it to perceive and interact with its surroundings.
- The robot's perception module integrates with ROS 2's sensor_msgs to receive data from cameras or other sensors, and uses image processing techniques to detect objects.
- Once an object is detected, the robot's planning module utilizes ROS 2's navigation and manipulation capabilities to determine an optimal pick and place trajectory.
- The robot's control module leverages ROS 2's control_msgs to send commands to its actuators, enabling precise and coordinated movement during pick and place operations.
Overall, the ROS 2-based humble pick and place robot with object detection demonstrates the power and flexibility of ROS 2 in enabling advanced perception, planning, and control capabilities for robotic systems.
