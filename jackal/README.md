## Jackal
This directory includes all files related to Clearpath Jackal robot including sensor integration, navigation and mapping.  

## Prerequisites:
Firstly, clone this repository.<br>

Type the following commands in the terminal to install the required dependencies:
```
sudo apt-get install ros-noetic-jackal-simulator
sudo apt-get install ros-noetic-jackal-*
sudo apt-get install ros-noetic-velodyne-*
sudo apt-get install ros-noetic-geodesy ros-noetic-pcl-ros ros-noetic-nmea-msgs ros-noetic-libg2o
sudo pip install ProgressBar2
sudo apt-get install ros-noetic-velodyne
sudo apt-get install ros-noetic-velodyne-simulator
sudo apt-get install ros-noetic-geographic-info
sudo apt-get install ros-noetic-robot-localization
sudo apt-get install ros-noetic-twist-mux
sudo apt-get install ros-noetic-pointcloud-to-laserscan
sudo apt-get install ros-noetic-teb-local-planner
rosdep install teb_local_planner
sudo apt-get install ros-noetic-stage-ros
```
<br>

Clone the following repositories 
```
git clone https://github.com/jackal/jackal.git
git clone https://github.com/jackal/jackal_desktop.git
git clone https://github.com/jackal/jackal_simulator.git
git clone https://github.com/OctoMap/octomap_mapping.git
```

Follow the steps to install the worlds
```
git clone https://github.com/clearpathrobotics/cpr_gazebo.git
```

## Sensor Mounting
 Refer to the following link to access various sensors - [Sensors](https://www.clearpathrobotics.com/assets/guides/melodic/jackal/description.html)
 <div style="display: flex; align-items: center;">
  <img src="./1.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p>.</p>
</div>
<div style="display: flex; align-items: center;">
  <img src="./2.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p>.</p>
</div>
<div style="display: flex; align-items: center;">
  <img src="./3.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p>.</p>
</div>
<div style="display: flex; align-items: center;">
  <img src="./4.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p>.</p>
</div>

## Visualisation
1. Depth Camera
   <div style="display: flex; align-items: center;">
  <img src="./depthcam.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p>.</p>
</div>
3. Stereo Camera
<div style="display: flex; align-items: center;">
  <img src="./octomap.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p>.</p>
</div>
4. 3D Lidar - Velodyne
<div style="display: flex; align-items: center;">
  <img src="./velodyne.png" alt="Jackal Robot" width="500" style="float: centre; margin-right: 20px;">
  <p>.</p>
</div>

## OCTOMAP
1. Probabilistic Mapping Framework: OctoMap is a probabilistic 3D mapping framework used in robotics and computer graphics. It represents environments as an octree, assigning probabilities to voxels (3D grid 
   cells) to indicate occupancy likelihood.

2. Sensor Fusion and Noise Handling: OctoMap excels at fusing data from multiple sensors, such as lidar and depth cameras. Its probabilistic approach effectively handles sensor noise and uncertainties, resulting 
   in accurate and adaptable maps.

3. Collision-Free Path Planning: By distinguishing between occupied and free spaces, OctoMap enables collision-free navigation. It's particularly valuable for robots moving in cluttered or dynamic environments, 
   aiding in safe path planning.

4. Unmapped Area Exploration: OctoMap identifies areas with uncertain occupancy, signaling unexplored regions. This encourages robots to autonomously explore and map unknown territories, contributing to 
   comprehensive environment mapping.

5. Memory and Efficiency: OctoMap balances detailed representation with memory efficiency. It optimizes storage by utilizing an octree structure, allowing for high-resolution maps without excessive memory usage. 
   Efficient access to map data supports real-time applications
## Steps to save octomap
```
roslaunch octomap_server octomap_mapping.launch
rosrun octomap_server octomap_saver my_octomap.bt
```
<br>

https://github.com/git-suwalkaaditya/RoughTerrain-IVR2/assets/108211492/7c40de8f-0589-4d52-a075-aeca3fb8680b


