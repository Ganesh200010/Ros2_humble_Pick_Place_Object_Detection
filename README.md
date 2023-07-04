<p align="left">

<img src="https://img.shields.io/badge/Ubuntu-22.04-orange.svg" alt="Ubuntu 22.04">
<img src="https://img.shields.io/badge/Python-3.x-blue.svg?logo=python&logoColor=white">
<img src="https://img.shields.io/badge/YOLO-v5-darkgreen?style=flat-square&logo=Yolo&logoColor=white">
<img src="https://img.shields.io/badge/Gazebo-v11-darkorange?style=flat-square&logo=&logoColor=white">
<img src="https://img.shields.io/badge/Rviz-v2-darkgreen?style=flat-square&logo=&logoColor=white">



</p>

# Ros2_humble

ROS2 (Robot Operating System 2) is a flexible framework for developing robotic systems. It provides a set of tools, libraries, and conventions that aid in building robot applications. ROS2 is designed to be more scalable, distributed, and real-time capable compared to its predecessor, ROS.


  
# 1.1 Pick & Place
Pick-and-place is a common robotic task where a robot arm picks up an object from one location and places it in another. The arm's movement can be controlled using inverse kinematics, which involves calculating the joint angles required to achieve a desired end-effector position




# 1.2 Object Detection

Object detection is the process of identifying and locating objects within an image or a point cloud. ROS2 provides several packages and libraries that can be used for object detection tasks

-	Ensure proper sensor calibration to achieve accurate object detection results.

<p align="left">


   <a href="https://github.com/Ganesh200010/Ros2_humble_Pick_Place_Object_Detection/assets/125490197/6a6360ac-386e-41fe-959f-27148435774c" target="blank"><img align="center" src="https://img.shields.io/badge/video-%230077B5.svg?style=for-the-badge&logo=video&logoColor=white" alt="https://github.com/Ganesh200010/Ros2_humble_Pick_Place_Object_Detection/assets/125490197/6a6360ac-386e-41fe-959f-27148435774c" /></a>

</P>



# 2. Environment Setup
   
The project uses [ROS2 Humble](https://docs.ros.org/en/humble/index.html) running on [Ubuntu 22.04.2 LTS (Jammy Jellyfish)](https://releases.ubuntu.com/jammy/)

The following tools are used for simulation and motion planning:

- [Gazebo](https://gazebosim.org/home): A physics-based 3D simulator extensively used in the robotics world.
- [RViz](http://wiki.ros.org/rviz): A 3D visualizer for sensor data analysis and robot state visualization.


# ⚙️ Commands 2 Implement

    
-  Create a directory structure as <code>ros2_ws/</code>.
        
        mkdir -p ros2_ ws

- The command "cd src" to change the current directory to a directory named <code>"src"</code> within the current working directory.
        
        cd src

-  Building and installs it with symbolic links <code>(Colcon)</code>.
        
        colcon build --packages-select ros2_ws/ --symlink-instal

- Install some dependencies and necessary packages:

      sudo apt instal/ python3-vcstoo/
      sudo apt instal/ ros-humble-test-msgs
      sudo apt instal/ ros-humble-contro/-too/box
      sudo apt instal/ ros-humble-gazebo-ros-pkgs 
      sudo apt instal/ ros-humble-xacro
      sudo apt instal/ ros-humble-joint-state-publisher-gui        


- **Then you need to download and build in your workspace the following packages**
  -  ros2_control framework
  -  gazebo_ros2_contro

-  Make sure to install these packages FROM SOURCE, and point to the correct branch otherwise, some problems could appear. Now you can clone our repository in your workspace and build the whole workspace. 

- **Now open a new terminal and write the following lines:**

      cd ros2_ws
      install/setup.bash
      ros2 launch my_doosan_pkg my_doosan_gazebo.launch.py
  
- **Open another new terminal and write the following lines:**

        cd ros2_ws
        install/setup.bash
        ros2 launch my_doosan_pkg my_doosan_rviz.launch.py
- For motion planning
          
       ros2 launch my_doosan_pkg my_doosan_gazebo_controller.launch.py

- ****Yolo****

- Now open a new terminal and write the following lines to launch <code>yolobot_gazebo yolobot_launch</code>

      source yolobot/install/setup.bash
      ros2 launch yolobot_gazebo yolobot_launch.py 
- Now open another terminal and write the following lines for <code>Yolov8_Inference</code>

      source yolobot/install/setup.bash
      ros2 topic list
      ros2 topic echo /Yolov8_Inference
- Following with <code>RVIz</code>

      rviz2

- In another terminal run <code>yolobot_recognition yolov8_ros2_subscriber</code>
  
      source yolobot/install/setup.bash
      ros2 run yolobot_recognition yolov8_ros2_subscriber.py 



## 3. Working

- The ROS2 based humble pick and place robot utilizes the ROS2 framework for communication and coordination between its components.
- It employs object detection algorithms to identify objects in its environment, enabling it to perceive and interact with its surroundings.
- The robot's perception module integrates with ROS2's sensor_msgs to receive data from cameras or other sensors, and uses image processing techniques to detect objects.
- Once an object is detected, the robot's planning module utilizes ROS2's navigation and manipulation capabilities to determine an optimal pick and place trajectory.
- The robot's control module leverages ROS2's control_msgs to send commands to its actuators, enabling precise and coordinated movement during pick and place operations.
Overall, the ROS2 based humble pick and place robot with object detection demonstrates the power and flexibility of ROS2 in enabling advanced perception, planning, and control capabilities for robotic systems.
