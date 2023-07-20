# 🤖 Welcome to the QBot GitHub Repository! 🚀

<h2>Description</h2>
QBot is a ROS2-based robot equipped with four wheels, encoders, an IMU, and a LiDAR. This robot is designed to provide smooth and precise omnidirectional motion using the mecanum wheel mechanism, and it utilizes data fusion from encoders and the IMU to calculate accurate odometry. With navigation2 (nav2) and SLAM capabilities, the robot can autonomously move from point A to point B, while incorporating linear y-motion for enhanced spatial awareness.

**<h2>Features:</h2>**
- Mecanum wheels for omnidirectional movement.
- Data fusion from encoders and IMU for precise odometry.
- Navigation2 (nav2) for point-to-point autonomous navigation.
- SLAM functionality with linear y-motion support.

**<h2>Installation:</h2>**

**1. Prerequisites:**
- Ubuntu 20.04 (Focal Fossa) or later
- ROS2 Foxy Fitzroy or Humble Hawksbill (with desktop or desktop-ros-base installation)

### Set Up the ROS2 Workspace
```bash
# Create and initialize the ROS2 workspace
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws
colcon build
source install/setup.bash
```

### Clone the Humble Mecanum Robot Repository
```bash
cd ~/ros2_ws/src
git clone https://github.com/your-username/humble_mecanum_robot.git
```

### Install Dependencies
```bash
cd ~/ros2_ws
rosdep install --from-paths src --ignore-src --rosdistro foxy -y
```

### Build the Workspace
```bash
cd ~/ros2_ws
colcon build
```

### Source the Workspace
```bash
source install/setup.bash
```

## Running the Robot

### Launch Navigation2 and SLAM
```bash
# Assuming you have a map for SLAM
ros2 launch humble_mecanum_robot navigation_slam_launch.py
```

### Move the Robot
```bash
# Send a goal to the robot using the Nav2 planner
ros2 run nav2_planner_cli nav2_planner_cli --goal x y theta
```

### Teleoperate the Robot (Optional)
```bash
# If you want to manually control the robot using the keyboard
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```

## Contributing
We welcome contributions to improve the Humble Mecanum Robot! If you want to add new features, fix bugs, or enhance the existing codebase, feel free to create pull requests.

## Issues
If you encounter any issues, please open an issue on the GitHub repository. We'll do our best to address it promptly.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

Embark on an exciting journey with the Humble Mecanum Robot! Happy coding and exploring! 🤖🌍
