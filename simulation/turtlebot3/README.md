# TurtleBot3 Simulation (ROS 2 Humble)

## Environment
- **OS**: Ubuntu 22.04 LTS (Jammy)
- **ROS 2**: Humble Hawksbill

## Commands Used
```bash
# Set TurtleBot3 model
export TURTLEBOT3_MODEL=burger

# Launch Gazebo simulation
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py

# Run teleop (in a new terminal)
ros2 run turtlebot3_teleop teleop_keyboard

# Launch RViz2 (in a new terminal)
ros2 launch turtlebot3_bringup rviz2.launch.py

# List active topics
ros2 topic list

# Check ROS 2 distro
printenv | grep ROS_DISTRO used instead of ros2 --version as the latter 
didn't show in output after the command

# Wrong ROS version initially
System has ROS2 Foxy and was removed and ROS2 Humble was installed

#Upgrading Ubunto
System OS was Ubunti 20.04 and was upgraded to 22.04 

#Robot not moving with teleop
Teleop was running after using command export TURTLEBOT3_MODEL=burger

#Robot not showing in RViz2
Initially RViz2 was empty. Fixed by setting Fixed Frame = odom and adding
RobotModel and LaserScan displays

#ROS installation errors (missing middleware)
Encountered librmw_cyclonedds_cpp.so not found. Fixed by reinstalling with:
sudo apt install ros-humble-rmw-cyclonedds-cpp -y

#GitHub authentication failed (password not supported)
Fixed by creating a Personal Access Token (PAT) and 
configuring Git credentials.

#Empty folders not showing on GitHub:Realized Git ignores empty directories.
Realized Git ignores empty directories. Fixed by ensuring 
files (screenshots + .rviz config) were saved and renamed before commit.
