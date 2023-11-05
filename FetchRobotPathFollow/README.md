
# Fetch Robot following the path project for group project 1 group 11

## Overview

This repository contains complete fetch robot following the path project. Code was done in python as team felt more comfortable using the language and found it much more straight forward than C++. The project uses ROS (Robot Operating System) and Gazebo for simulation.

## Structure

- `src/`: Contains the Python source code for the ROS nodes.
- `launch/`: Contains the ROS launch files.
- `worlds/`: Contains the Gazebo world files.
- `models/`: Contains the 3D models for the simulation.

## Authors and Contributions 

Amer Abu-Issa
  - Obstacle Detection
  - Repository Setup
  - Documentation
  - Guider follow and control

Elijah Mayhew
   - Environment Setup (Environment Sensing)
   - Controller teleop node (Guider Control)
   - Demo Video (simulation problems)
   - Documentation

Rosemary Tawdrous
  - Laser detection 
  - Laser Scan
  - Aruco Marker Detection
  - Documentation

## Prerequisites

- Python 3.x / Python
- ROS melodic (or compatible version)
- Gazebo


## Dipendencies 

Have Fetch Packages installed and Turtlbot package installed into the catkin workspace before installation. package and simulation will build on these dependencies.

Aruco Marker Detection used to detect the guider robot. Install  aruco marker detection. (https://github.com/pal-robotics/aruco_ros.git) created for easy install and can be utilised in catkin_ws/src directory.

## Expected Outcome

The turtlebot will act as guider robot and traverse through environment while the fetch robot will follow. As long as AR marker is seen by fetch RGBD camera then it will continue. If marker cannot be seen by fetch robot it will stop and wait for the guider to move to a location for fetch robot view before resuming the following operation. Fetch robot will cease following and wait for guider to relocate if obstacle is interfering. 

## Achieved Outcome

The simulation in Gazebo was a very difficult process to get up. To begin our initial issue was the turtlebot would not load up into the environment even with numerous trials and errors. After fixing the issue gazebo on our laptops would not be able to simulate world due to limitation of hardware. A group member even tried using his desktop PC instead of laptop which had a very strong graphic card and overall components. Gazebo had trouble loading in due to graphic card not being compatible with simulation requirements. We tried to work on laptops again however fps was too low and time was running out. By the time we had finished working on code we didn't have much time simulating and didn't realise we would encounter such simulation issues with gazebo constantly crashing and working at times. We have  a video to show for it without the environment completely initialised and turtlebot missing due to gazebo not simulating it. These reasons are unknown to us and we believe it is a Gazebo issue.


## Installation 


1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/yourrepository.git
    ```

2. Navigate to the project directory:

    ```bash
    cd yourrepository
    ```

3. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Build the ROS package:

    ```bash
    catkin_make
    ```

## Usage

1. Source the ROS workspace:

    ```bash
    source devel/setup.bash
    ```

2. Launch the simulation:

    ```bash
    roslaunch your_package your_launch_file.launch
    ```