**GitHub Repository: QBot**

**Description:**
Welcome to the GitHub repository of the Humble Mecanum Robot, a ROS2-based robot equipped with four wheels, encoders, an IMU, and a LiDAR. This robot is designed to provide smooth and precise omnidirectional motion using the mecanum wheel mechanism, and it utilizes data fusion from encoders and the IMU to calculate accurate odometry. With navigation2 (nav2) and SLAM capabilities, the robot can autonomously move from point A to point B, while incorporating linear y-motion for enhanced spatial awareness.

**Features:**
- Mecanum wheels for omnidirectional movement.
- Data fusion from encoders and IMU for precise odometry.
- Navigation2 (nav2) for point-to-point autonomous navigation.
- SLAM functionality with linear y-motion support.

**Installation:**

**1. Prerequisites:**
- Ubuntu 20.04 (Focal Fossa) or later
- ROS2 Foxy Fitzroy or Humble Hawksbill (with desktop or desktop-ros-base installation)

**2. Set Up the ROS2 Workspace:**
```bash
# Create and initialize the ROS2 workspace
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws
colcon build
source install/setup.bash
```

**3. Clone the Humble Mecanum Robot Repository:**
```bash
cd ~/ros2_ws/src
git clone https://github.com/your-username/humble_mecanum_robot.git
```

**4. Install Dependencies:**
```bash
cd ~/ros2_ws
rosdep install --from-paths src --ignore-src --rosdistro foxy -y
```

**5. Build the Workspace:**
```bash
cd ~/ros2_ws
colcon build
```

**6. Source the Workspace:**
```bash
source install/setup.bash
```

**Running the Robot:**

**1. Launch Navigation2 and SLAM:**
```bash
# Assuming you have a map for SLAM
ros2 launch humble_mecanum_robot navigation_slam_launch.py
```

**2. Move the Robot:**
```bash
# Send a goal to the robot using the Nav2 planner
ros2 run nav2_planner_cli nav2_planner_cli --goal x y theta
```

**3. Teleoperate the Robot (Optional):**
```bash
# If you want to manually control the robot using the keyboard
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```

**Contributing:**
We welcome contributions to improve the Humble Mecanum Robot! If you want to add new features, fix bugs, or enhance the existing codebase, feel free to create pull requests.

**Issues:**
If you encounter any issues, please open an issue on the GitHub repository. We'll do our best to address it promptly.

**License:**
This project is licensed under the MIT License. See the LICENSE file for more details.

Get ready to explore the world with the Humble Mecanum Robot! Happy coding! 🚀
