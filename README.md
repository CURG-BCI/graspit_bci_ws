# BCI User Interface
Top level repo for BCI Graspit Project

### Automatically installed by wstool during setup:
- See the ```.rosinstall``` file for a list of these.

## Setup
The following is the procedure to set up the workspace for the Shape Completion project.

1. Install ROS and Graspit dependencies.
 ```
  http://wiki.ros.org/indigo/Installation/Ubuntu
  http://www.cs.columbia.edu/~cmatei/graspit/html-manual/graspit-manual_2.html#id1
  ```
  
2. Clone this repository into your workspace.

  ```
  git clone https://github.com/CURG-BCI/graspit_bci_ws.git
  cd graspit_bci_ws/src
  ```
3. Run wstool update. This will clone all the other dependent repositories listed in the .rosinstall file into that workspace
  
  ```
  wstool update
  ```
  
4. Initialize the ROS workspace
  
  ```
  source /opt/ros/indigo/setup.bash
  cd src
  catkin_init_workspace
  ```
  
5. Change the version of graspIt! to the bci project version it only has small changes, a new world file and default configurations for building.
  
  ```
  cd /src/grasit-ros/graspit
  rm -rf graspit_source 
  git clone https://github.com/CURG-BCI/graspit.git graspit_source
  ```
  
6. Build project:

  ```
  cd graspit_bci_ws
  source /opt/ros/indigo/setup.bash
  catkin_make
  ```
7. run project:

  ```
  source devel/setup.bash
  roslaunch graspit_bci_plugin ros_graspit_interface.launch
  ```
