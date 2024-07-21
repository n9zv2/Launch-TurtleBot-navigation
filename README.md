# Launch-TurtleBot-navigation

## Introduction

The TurtleBot Navigation package enables your TurtleBot to perform autonomous navigation tasks. This includes:

- **Localization**: Determining the robot's position within a map.
- **Mapping**: Creating a map of the environment.
- **Path Planning**: Computing the best path to navigate from one point to another.
- **Obstacle Avoidance**: Detecting and avoiding obstacles in the environment.


### Image 1: Creating the `demo` Package
![cratet_pakeges](https://github.com/user-attachments/assets/2b7ca2b2-05c6-417c-a5cd-950f2200ea7b)


- **Command Executed:** `catkin_create_pkg demo std_msgs rospy roscpp`
- **Description:** This command creates a new ROS package named `demo` with dependencies on `std_msgs`, `rospy`, and `roscpp`. The output shows the successful creation of necessary files (`package.xml`, `CMakeLists.txt`) and directories (`include/demo`, `src`). The prompt to adjust the values in `package.xml` indicates that the package has been initialized.


### Image 2: Installed Packages

![install all pagege](https://github.com/user-attachments/assets/c2dc74e1-c7a8-4349-9dd3-cea46c11ba76)

- **Description:** This image shows the traversal of 12 packages in topological order. These packages are part of the TurtleBot3 ecosystem and include `turtlebot3`, `turtlebot3_msgs`, `turtlebot3_navigation`, `turtlebot3_simulations`, and others, along with the newly created `demo` package.

### Image 3: RViz Visualization


![map2](https://github.com/user-attachments/assets/62dc1b88-61de-46e5-859d-f88d515312aa)

- **Description:** This image displays the RViz interface with the TurtleBot3 navigation stack loaded. Various displays such as Grid, RobotModel, LaserScan, and Map are shown. The global status has an error, and the map status is in a warning state, suggesting some configuration issues or missing data.


### Image 3: Empty map

![lunshMap](https://github.com/user-attachments/assets/0170379a-f73e-4a75-8e5b-636e5e689c5b)

 **Description:** A placeholder map with no obstacles or features, used for initializing navigation systems or testing algorithms in an unstructured environment.



 ## Setup TurtleBot3 Packages

1. **Update and Upgrade System Packages**

    ```bash
    sudo apt-get update
    sudo apt-get upgrade
    ```

2. **Clone TurtleBot3 Repositories**

    Navigate to the `src` directory of your Catkin workspace:

    ```bash
    cd ~/catkin_ws/src/
    ```

    Clone the necessary TurtleBot3 repositories:

    ```bash
    git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git -b noetic-devel
    git clone https://github.com/ROBOTIS-GIT/turtlebot3.git -b noetic-devel
    ```

3. **Build the Workspace**

    Return to the root of your Catkin workspace and build it:

    ```bash
    cd ~/catkin_ws
    catkin_make
    ```

## Setup TurtleBot3 Simulations

1. **Clone TurtleBot3 Simulation Repository**

    Navigate to the `src` directory of your Catkin workspace:

    ```bash
    cd ~/catkin_ws/src/
    ```

    Clone the TurtleBot3 simulation repository:

    ```bash
    git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
    ```

2. **Build the Workspace Again**

    Return to the root of your Catkin workspace and build it:

    ```bash
    cd ~/catkin_ws
    catkin_make
    ```

## Launch TurtleBot3 in Gazebo

To launch TurtleBot3 in an empty Gazebo world, use the following command:

```bash
roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch

