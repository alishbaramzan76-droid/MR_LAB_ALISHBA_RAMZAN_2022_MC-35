Week 1 lab focused on learning the basics of Linux and understanding core ROS 2 concepts. We verified the ROS 2 Humble installation, practiced terminal navigation, and learned important terms such as node, topic, package, and workspace.

We created a ROS 2 workspace (ros2_ws) and built it using colcon build. Inside the workspace, we created a Python package named my_first_pkg. We then implemented a simple node (simple_node) that prints a message using ROS logging.

We registered the node as an executable using the entry_points section in setup.py, rebuilt the workspace, and successfully ran the node using ros2 run.

This lab established the foundation for ROS 2 development, including workspace management, package creation, building, sourcing, and executing nodes.

**Commands used:**

**Linux Basic Commands**
pwd

ls

ls -l

cd ~

cd /

mkdir -p ~/practice_linux/subfolder

cd ~/practice_linux

cd ..

nano test.txt

gedit test.txt

**ROS 2 Verification Commands**

source /opt/ros/humble/setup.bash

printenv | grep -E "ROS|RMW|AMENT"

**Workspace Creation Commands**

mkdir -p ~/ros2_ws/src

cd ~/ros2_ws

colcon build

source install/setup.bash

echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc

echo "source ~/ros2_ws/install/setup.bash" >> ~/.bashrc

source ~/.bashrc

ls

**Package Creation Commands**

cd ~/ros2_ws/src

ros2 pkg create --build-type ament_python my_first_pkg

ros2 pkg list | grep my_first_pkg

**Editing & File Permissions**

nano ~/ros2_ws/src/my_first_pkg/my_first_pkg/simple_node.py

chmod +x ~/ros2_ws/src/my_first_pkg/my_first_pkg/simple_node.py

nano ~/ros2_ws/src/my_first_pkg/setup.py

**Build and Run Commands**

cd ~/ros2_ws

colcon build

source install/setup.bash

ros2 run my_first_pkg simple_node

ros2 node list
