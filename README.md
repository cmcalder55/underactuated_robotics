# Underactuated Robotic Gripper
Underactuated robotic gripper research performed through the Advanced Robot Manipulators Laboratory at Stevens Institute of Technology under the guidance of Dr. Long Wang. View the lab webpage here: https://longwang.in/

BACKGROUND: This project was focused on creating a low-cost robotic hand that can be attached to a commercial robotic arm for various complex manipulation tasks. The main feature of the design is the underactuation system, meaning multiple joints can be controlled by one mechanism. Inspired by human biology, tendon-driven underactuation is used to control 8 finger joints using only 2 motors.The manipulator can be positioned and commanded directly by a user. The manipulator uses force and angle sensors to optimize its grasp. Tasks can also be performed autonomously using sensor feedback.  
![alt text](https://github.com/cmcalder55/underactuated_robotics/blob/main/screenshots/davinci.jpg?raw=true)  
SIMULATION: First, a SolidWorks model of the robotic hand was created. Once the model was approved, a physical prototype was created and attached to a Kinova robotic arm. 
https://youtube.com/shorts/SLhP_C6LJS4?feature=share 
The SolidWorks model was converted to a URDF (Unified Robot Description Format). The URDF model was loaded into the robot simulator program Gazebo and attached to a Kinova arm model (available on their website). For initial testing, a model of a soda can was used as the target.  
ROS code was then written to define each link and joint of the system. Through a RViz controller GUI, the inertia of each joint can then be adjusted using a slider or direct numeric inputs.   

![alt text](https://github.com/cmcalder55/underactuated_robotics/blob/main/screenshots/overhead.png?raw=true)

After choosing the desired end position, a path planning algorithm is used to find the shortest and smoothest path. After the gripper is positioned, it tightens around the object until it receives sufficient force feedback to try and pick up the object. The joint positions and inertias can then be adjusted to optimize its path and grip strength. 
https://youtu.be/HWir0G_nYKU 

When the robot was able to successfully pick up the can, further tests were run using a cube and a door handle. This was done to ensure the robot could adjust to a variety of target geometries and angles. This also helped to ensure the simulation modeled the physical sensors correctly, since the manipulation task could also be run in real time with the same commands on the physical system.  

