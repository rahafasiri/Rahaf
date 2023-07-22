# Install ROS on VirtualBox
![صورة النظام في الفيرشوال بوكس](https://github.com/rahafasiri/Rahaf/assets/139389205/2dbc7072-1aeb-40bd-bf4a-ed0fa9869aab)
## Executing commands
![excution commands](https://github.com/rahafasiri/Rahaf/assets/139389205/6231665f-0df9-4b27-ab63-4b164d5cd8f4)
![excution commands 2](https://github.com/rahafasiri/Rahaf/assets/139389205/d486891a-cf1c-47ef-8265-5adfe12eca6c)

### These commands are used to install and configure ROS (Robot Operating System) and then create a workspace to work on a specific ROS package called "arduino_robot_arm". Here is a brief explanation for each command:

1. `sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'`: This command adds the ROS repository to the system's package manager sources list.

2. `sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654`: This command adds the ROS repository key to the system's apt keyring.

3. `sudo apt-get update`: This command updates the system's package manager with the new ROS repository.

4. `sudo apt-get install ros-kinetic-desktop-full`: This command installs the full version of the ROS kinetic release.

5. `apt-cache search ros-kinetic`: This command searches for available ROS packages for the kinetic release.

6. `echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc`: This command adds a line to the bashrc file to source the ROS setup script when a new terminal is opened.

7. `source ~/.bashrc`: This command reloads the bashrc file to activate the changes made in step 6.

8. `sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential`: This command installs additional tools and dependencies for working with ROS packages.

9. `sudo apt install python-rosdep`: This command installs the ROS dependency manager.

10. `sudo rosdep init`: This command initializes the rosdep tool.

11. `rosdep update`: This command updates the rosdep database.

12. `sudo apt-get install ros-noetic-catkin`: This command installs the catkin package, which is used to build ROS packages.

13. `mkdir -p ~/catkin_ws/src`: This command creates a new workspace directory for our ROS package.

14. `cd ~/catkin_ws/`: This command navigates to the newly created workspace.

15. `catkin_make`: This command initializes the catkin workspace.

16. `cd ~/catkin_ws/src`: This command navigates to the src directory of the workspace.

17. `git clone https://github.com/smart-methods/arduino_robot_arm.git`: This command clones the arduino_robot_arm package from GitHub.

18. `cd ~/catkin_ws`: This command navigates back to the catkin workspace directory.

19. `rosdep install --from-paths src --ignore-src -r -y`: This command installs the dependencies for the arduino_robot_arm package.

20. `sudo apt-get install ros-kinetic-moveit`: This command installs the MoveIt! package, which is used for motion planning.

21. `sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui`: These commands install the joint_state_publisher and joint_state_publisher_gui packages, which are used to publish joint states.

22. `sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher`: These commands install the Gazebo simulator and its ROS control plugin.

23. `sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control`: These commands install the ROS controllers and ROS control packages, which are used for controlling the robot arm.

24. `sudo nano ~/.bashrc`: This command opens the bashrc file for editing.

25. At the end of the bashrc file, add the following line: `source /home/wesam/catkin_ws/devel/setup.bash`. This command sources the ROS setup script for the arduino_robot_arm package.

26. `ctrl + o`: This command saves the changes made to the bashrc file.

27. `source ~/.bashrc`: This command reloads the bashrc file to activate the changes made in step 25.

28. `roslaunch robot_arm_pkg check_motors.launch`: This command launches the check_motors.launch file, which checks the motors of the robot arm.
#### Arm implementation on the emulator
![صورة الذراع ](https://github.com/rahafasiri/Rahaf/assets/139389205/8abfa470-3bd7-457a-add5-6b110746eea9)
