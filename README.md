# turtlesim package in ROS
The **turtlesim** package is a popular tool for learning ROS (Robot Operating System) concepts, particularly for beginners. It provides a simple simulator where you can control a turtle in a 2D environment.  
Below, I'll guide you through the steps to use the turtlesim package in both ROS Noetic and ROS Foxy.
### Prerequisites
- ROS Noetic is built on top of Ubuntu 20.04 and is compatible with Python 3.
- ROS Foxy is built on top of Ubuntu 20.04 and is part of ROS 2.
## Turtlesim in ROS Noetic
### Step 1: Initialize ROS Master
Open a terminal and run the following command:
```sh
roscore
```
The output should be like this: 
<p align = "center">
  <img src="https://github.com/user-attachments/assets/3f25188f-2538-42f5-aeb5-1430a4714db4" width="750">
</p>
If you find any errors and do not get the same output as in the previous image, make sure that you set up the environment using the following command before anything related to ROS noetic :  

```sh
source /opt/ros/noetic/setup.bash
```

### Step 2: Launch Turtlesim Node
Open a new terminal and run:
```sh
rosrun turtlesim turtlesim_node
```
This will open a window with a turtle in a 2D environment like this :
<p align = "center">
  <img src="https://github.com/user-attachments/assets/a660fe60-012c-4a0e-956a-2487679003d5" width="750">
</p>

### Step 3: Move the Turtle
Open another terminal and run the turtle_teleop_key node to control the turtle using your keyboard:
```sh
rosrun turtlesim turtle_teleop_key
```
Use the arrow keys to move the turtle around.  
- **note :** Make sure you are on the same terminal as the command because if you click anywhere else and use the arrows the turtle will not move.
![Screenshot 2024-07-29 124006](https://github.com/user-attachments/assets/2fd8c40a-32f3-448a-92eb-5b82d0e0dfe7)

### More commands 
if you write **'rosrun turtlesim'** in terminal and Double-click the **Tab** button you will see the rest of the commands that can be used, such as:  
- draw_square
- mimic
- turtlesim_node  
For more information visit [turtlesim](https://wiki.ros.org/turtlesim).

## Turtlesim in ROS Foxy
In ROS 2 (Foxy), the process is slightly different due to changes in architecture and tools.
### Step 1: Source the ROS 2 Environment
```sh
source /opt/ros/foxy/setup.bash
```
### Step 2: Launch Turtlesim Node
```sh
ros2 run turtlesim turtlesim_node
```
You'll see the turtlesim window:  

![Screenshot 2024-07-29 130607](https://github.com/user-attachments/assets/6394e480-d686-432b-87b8-fd5c79b3491f)

### Step 3: Move the Turtle
In another terminal, run the teleop node:
```sh
ros2 run turtlesim turtle_teleop_key
```
Use the arrow keys to control the turtle.  

![Screenshot 2024-07-29 131301](https://github.com/user-attachments/assets/72f0373a-ffa4-4f2b-b782-007949bb07db)

### Step 4: Interact with Turtlesim using ROS 2 Commands
#### List available services:
```sh
ros2 service list
```
#### Call a service to reset the turtle:
```sh
ros2 service call /reset std_srvs/srv/Empty
```
![Screenshot 2024-07-29 134327](https://github.com/user-attachments/assets/367d7ce9-dfa2-469d-bdf5-956f8a3fb803)


