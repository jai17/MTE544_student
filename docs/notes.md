# To launch gazebo

```bash
ros2 launch turtlebot3_gazebo turtlebot3_house.launch.py
```

# Teleop control

```bash
ros2 run turtlebot3_teleop teleop_keyboard
```

# RViz Map and Goal Pose

```bash
python3 mapPublisher.py
rviz2 -d pathPlanner.rviz
python3 decisions.py
```

# Mapping in simulation

```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=True
ros2 run nav2_map_server map_saver_cli -f ~/map
```

# To check latency

```bash
./latency_check.py topic msgType
# for example for scan topic
./latency_check.py /scan LaserScan
```

# To view TF tree

```bash
ros2 run tf2_tools view_frames
ros2 run tf2_ros tf2_echo [source_frame] [target_frame]
```

# Every time in a new terminal

```bash
source ~/robohub/turtlebot4/configs/.bashrc
export ROS_DOMAIN_ID=X # x is the number of the robot
```