# MATLAB
This project involves using Mathworks softwares for implementing a robust and efficient rough terrain navigation system using the Navigation, Robotics System, Image Processing, Automated Driving and ROS Toolbox in MATLAB. This project aims to enable autonomous robots to navigate challenging terrains, such as rocky surfaces, uneven landscapes, and rugged environments.

## Installation:
1. Install Matlab R2022b - [MATLAB INSTALLATION](https://in.mathworks.com/downloads/) <br>
   While installing MATLAB, ensure that you install the following toolboxes:<br>
   a. Robotics System Toolbox<br>
   b. ROS Toolbox<br>
   c. Navigation Toolbox<br>
   d. Automated Driving Toolbox<br>
   e. Image Processing(Optional)<br>

2. Install ROS Noetic on your Ubuntu system - [ROS INSTALLATION](http://wiki.ros.org/noetic/Installation/Ubuntu).

## Features :
1. *Co-Simulation* - Setting up ROS-MATLAB co-simulation as a link for data transfer between the two. <br>
2. *Visualisation* -  Visually depicting the data received from sensors like 2D & 3D Lidar, depth cameras etc.<br>
3. *Global Path Planners* - Implemented various path planners like RRT, RRT* and Hybrid A*. <br>
4. *Localisation* - Applied Adaptive Monte Carlo Localization, a particle filter-based approach to estimate the robot's initial pose.<br>
5. *Motion Planning* - Developed a Simulink Model, which exploits the laser scan topic and /cmd_vel topic to move the bot along the given waypoints and demonstrate obstacle avoidance.<br>


## Co-simulation of ROS-MATLAB :
ROS MATLAB co-simulation enables seamless integration between MATLAB and ROS (Robot Operating System), facilitating real-time data exchange, control, and visualization, making it a powerful combination for developing and testing complex robotic systems and algorithms.
<div style="display: flex; align-items: center;">
  <img src="./rosinit.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p></p>
</div>
1. To perform Co-simulation, type in the IP address of the Linux system where you plan on running the Gazebo simulation files.<br>
2. If there are no errors in connection, the script proceeds to completion.<br>

## Visualisation :
MATLAB was used to receive sensor data from the Gazebo bot. This data was later visualised to enhance understanding.<br>
*2D Lidar*
<div style="display: flex; align-items: center;">
  <img src="./laserscan.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p></p>
</div>

*3D Lidar*
<div style="display: flex; align-items: center;">
  <img src="./3D_LIDAR.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p></p>
</div>

*rosbag file was recorded in the linux system and ROSbagfile viewer app(R2023a) was used to visualise the recorded data*
<br>

https://github.com/git-suwalkaaditya/RoughTerrain-IVR2/assets/108211492/a81afa7b-d3ac-43a7-9534-a46306feaea1

<br>

## Global Path Planners :
After thorough experimentation with various path planners, including RRT, RRT*, A*, and Hybrid A*, we present the results of our tests.<br>

_The occupancy map of the gazebo world is to be made from .pgm file. Refer to [2D Occupancy Map](https://in.mathworks.com/help/nav/ref/occupancymap.html?searchHighlight=occupancy%20map%202d&s_tid=srchtitle_support_results_1_occupancy%2520map%25202d)_<br>

*RRT*<br>
RRT (Rapidly-exploring Random Trees) Global Path Planner is a popular algorithm used in robotics and motion planning to efficiently search and construct feasible paths in complex, high-dimensional environments.<br>
<div style="display: flex; align-items: center;">
  <img src="./RRT.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p></p>
</div>

*RRT**<br>
RRT* (Rapidly-exploring Random Trees Star) Global Path Planner is an enhanced version of the RRT algorithm that optimizes the paths it generates by iteratively rewiring the tree, resulting in higher-quality and more optimal paths in complex environments.<br>
<div style="display: flex; align-items: center;">
  <img src="./RRTstar.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p></p>
</div>

*A**<br>
A* (A-star) Global Path Planner is a widely-used graph-searching algorithm that efficiently finds the shortest path from a start to a goal node, combining the advantages of both Dijkstra's algorithm and heuristics to ensure optimality and speed in various applications, including robotics and game development.<br>
<div style="display: flex; align-items: center;">
  <img src="./Astar.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p></p>
</div>

*Hybrid A**<br>
Hybrid A* Global Path Planner is an extension of the traditional A* algorithm that combines grid-based and sampling-based methods, allowing it to efficiently find feasible and smooth paths for autonomous vehicles in continuous state spaces, making it suitable for real-world navigation scenarios.<br>
<div style="display: flex; align-items: center;">
  <img src="./HybridAstar.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p></p>
</div>

## Localisation :
AMCL (Adaptive Monte Carlo Localization) is a probabilistic localization algorithm widely used in robotics and autonomous systems to accurately estimate the pose (position and orientation) of a robot within its environment, utilizing a particle filter approach that dynamically adjusts the number of particles to adapt to changing uncertainties.
<div style="display: flex; align-items: center;">
  <img src="./AMCL.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p></p>
</div>

## Motion Planning :
The simulink Model interfaces with a Robot Operating System (ROS) environment, receiving odometry and laser scan data. The model incorporates waypoints generated by path planners, enabling the robot to follow the desired path while implementing obstacle avoidance strategies, resulting in safe and efficient navigation through the environment.

## Matlab Scripts :
*1. Path planners :* <br>
      AstarPlanner.mlx<br>
      RRTPlanner.mlx<br>
      RRTstarPlanner.mlx<br>
      HybridAstarplanner.mlx<br>

*2. Transformations :*<br>
      AccessTF.mlx<br>

*3. Localisation :*<br>
      MonteCarlo.mlx<br>

*4. Motion Planning :*<br>
      PathFollowingWithObstacleAvoidanceInSimulink.mlx


<br>

https://github.com/git-suwalkaaditya/RoughTerrain-IVR2/assets/108211492/2fc75717-ea71-44f8-bb29-8db2674aa7eb
