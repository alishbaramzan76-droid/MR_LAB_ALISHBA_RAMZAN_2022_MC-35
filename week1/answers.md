1. Define: node, topic, package, workspace.

Node: A node iss aprogram that performs a service like a task for example read a sensor or control the motor

Topic: A communication channel where nodes send and receive messages

Package: A folder that holds Ros2 codes dependencies, and configuration files.

Workspace: Main folder that contains one or more ros2 packages and build files.

2. Explain why sourcing is required. What happens if you do not source a workspace?

Sourcing sets up environment variables so ROS 2 can find your packages and executables.

If you do not source the workspace, ROS 2 will not detect your package, and commands like ros2 run or ros2 pkg list will not work properly.

3. What is the purpose of colcon build? What folders does it generate?

colcon build compiles and installs your ROS 2 packages so they can run properly.

4. In your own words, explain what the entry_points console script does in setup.py.

The entry_points console script connects a command name to a Python function.

It tells ROS 2 which file and function to run when we type ros2 run package_name executable_name.


5. Diagram: One publisher and one subscriber connected by a topic.

+------------+        /example_topic        +-------------+
| Publisher  | ---------------------------> | Subscriber  |
|  Node A    |                              |   Node B    |
+------------+                              +-------------+

Node A sends messages to the topic.

Node B receives messages from the same topic.
