# ROS-TF-Introduction
This project implements the forward kinematics for a robot arm defined in a URDF file and running in a ROS environment.

## Getting Started
Download the folders and add them to your catkin folder.

```
Start your roscore: roscore

Import the description of the robot file :cd catkin_ws
rosparam set robot_description --textfile kuka_lwr_arm.urdf

Start the simulation: rosrun robot_sim robot_sim_bringup

Move the joints automatically: rosrun robot_mover mover
(you can listen to the joints values: rostopic echo /joint_states)
OR do it manually: rosrun robot_sim position_command.py

Execute the node computing the position of each links depending on the joints values: rosrun forward_kinematics forward_kinematics.py

Visualize the robot: rosrun rviz rviz
Then select in Fixed Frame "wolrd_link". Click Add and on the popup screen select "RobotModel". You can also add the item "TF" if you want to see a visual representation of the frames.
```


### Prerequisites
You need a complete installation of ROS.
I only tried on the melodic version of ROS.

### Results
![Image of a running example](/execution.png)

## Author
* **Mickaël Trezzy**
