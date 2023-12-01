# Ares Rover Simulation Project

## Overview

This project is a simulation of the OzUrover team's Ares Rover in Gazebo with ROS, featuring differential drive, motor plugins, and accurate 3D models, tailored for advanced robotic research and development.

## Installation

To run the Ares Rover simulation, follow these steps:

1. **Clone the Repository:**

    ```bash
    git clone [repository URL]
    cd [repository directory]
    ```

2. **Build the Workspace:**

    Ensure you have ROS and Gazebo installed, then run:

    ```bash
    catkin_make
    ```

3. **Source the Setup Script:**

    ```bash
    source devel/setup.bash
    ```

## Usage

To launch the Ares Rover simulation in Gazebo:

1. **Start the Simulation:**

    ```bash
    roslaunch ares_rover ares_rover_gazebo.launch
    ```

2. **Control the Rover:**

    The rover can be controlled using the motor plugins provided. Send commands to each wheel's topic, for example:

    ```bash
    rostopic pub /ares_rover/front_left_wheel/command std_msgs/Float64 "data: 1.0"
    ```

    Repeat for other wheels as needed.

## Project Structure 

- `urdf/ares_rover.urdf.xacro`: URDF file defining the rover's physical structure and properties.
- `launch/ares_rover_gazebo.launch`: Launch file to start the Gazebo simulation with the rover.
- `meshes/`: Folder containing STL files for the rover's visual and collision models.
