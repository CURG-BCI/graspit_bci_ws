# BCI User Interface
Top level repo for BCI Graspit Project

### Automatically installed by wstool during setup:
- See the ```.rosinstall``` file for a list of these.

## Setup
The following is the procedure to set up the workspace for the Shape Completion project.

1. Install the dependencies mentioned above under the subsection "Should be manually installed before setup."
2. Clone this repository into your workspace.

  ```
  git clone https://github.com/CURG-BCI/graspit_bci_ws.git
  cd graspit_bci_ws/
  ```
3. Run wstool update. This will clone all the other dependent repositories listed in the .rosinstall file into that workspace
  
  ```
  wstool update
  ```

4.  Source ros :

  ```
  source /opt/ros/indigo/setup.bash
  ```
  
5. Build project:

  ```
  catkin_make
  ```
5. run project:

  ```
  source devel/setup.bash
  roslaunch graspit_bci_plugin ros_graspit_interface.launch
  ```
