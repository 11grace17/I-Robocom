# Introduction
This engineer’s documentation comprises engineering materials of the autonomous vehicle robot’s model, designed for participation in the WRO Future Engineers Competition in 2024.

# Content
schemes This folder contains one or several schematic diagrams in the form of JPEG, PNG, or PDF of the electromechanical components illustrating all the elements (electronic components and motors) used in the vehicle and how they connect.

src This folder contains all the programming flowcharts and all programming used to participate in the WRO 2024 Future Engineers Category.

pictures-team & vehicle This folder contains photos of the team participating in the WRO, photos of the vehicle (from all sides and bottom views) and photo shown in documentation.

video This folder contains video.md file that demonstrates how the robot functions to solve both tasks.

models This folder contains the 3D design of the vehicle in .lxf and the rendered model of the vehicle.

other This folder contains other files which can be used to understand how to prepare the vehicle for the competition.

# I-Robocom Team, Malaysia
Our team, consisting of three dedicated members, meticulously manages vital aspects of the build. Here’s a brief introduction for team I-Robocom from Malaysia and an overview of the essential electromechanical components powering our fully autonomous vehicle. Let’s meet our team members: Nelson Soo Hui Leng, Chang Pei Ru and Grace Tan Hong Hui.
 
![image](https://github.com/user-attachments/assets/9b97fa88-97bf-43cb-a684-3b05c71ba12a)

# 1.0 Mobility Management
This section provides an overview of the robot’s design, detailing how its movement is controlled, along with the types of motors used. It includes a summary of the vehicle’s chassis design and how various components are mounted on the structure. Additionally, key engineering principles such as speed, torque, and power are discussed.

## 1.1 Design of the robot
The autonomous robot is constructed using the Lego 45544 Mindstorms EV3 Education Set. 
![image](https://github.com/user-attachments/assets/a3faa8c6-da3b-4916-b486-fa2adb304ab8)

## 1.2 	Chassis of the robot
The design of the vehicle's chassis plays a crucial role in providing structural support, which ensures the robot remains stable during fast movements like sharp turns and rapid accelerations. Therefore, our self-driving car is designed based on the selection of the tyre, the implementation of motors, the implementation of differential gear and the engineering principle of the steering.

(a)	Selection of tyre
We chose the LEGO 32019+86652 wheels because the 43.2 x 14 rubber tire (86652) provides strong grip on different surfaces, reducing slipping and improving stability. It allows our self-driving car to move in a stable way while encountered in both Open Challenge and Obstacle Challenge.

(b)	Implementation of motor and its engineering principle
We use two Medium Motors to move the robot forward and backward. By placing them side by side horizontally, or we known as laterally to save space and make the robot more compact. This setup also makes it easier to arrange the reduction gears and keeps the center of gravity low, which improves stability during high-speed movement or turns and reduces the risk of tipping.

![image](https://github.com/user-attachments/assets/ed2d1db9-f80f-4440-af76-af2387c30c43)
  ![image](https://github.com/user-attachments/assets/0e8f951f-af5b-4631-a99a-22a8a37a9a81)
  ![image](https://github.com/user-attachments/assets/0f8c650d-eaf5-4090-9382-294ddebbe9a5)



The diagram below show the details of the EV3 Medium Motor. 
![image](https://github.com/user-attachments/assets/0ab6104f-f4e0-4a4f-bc85-c1ea3a65089d)


The Medium Motor is built for quick reactions and precise movements. It’s great for tasks like steering a robot, where small adjustments are needed. With that, the running torque of 8 Ncm and a stalled torque of 15 Ncm allow the robot to handle moderate forces for the steering. With a speed of 260 rpm, the medium motor can rotate quickly, making it ideal for rapid changes in direction or fine adjustments.

(c)	Implementation of differential gear
The differential gear distributes power between two axles, allowing them to rotate at different speeds. This helps the robot make smooth turns, especially when navigating corners.

(d)	Engineering principle of steering
Our robot’s front steering uses a gear-down system, which slows down the turning motion for better control and precision in small rotations. This is especially helpful for making smooth, precise turns in smaller LEGO models.
We also use Ackermann steering geometry, which gives each front wheel a slightly different angle when turning. This setup allows the inner and outer tires to follow separate paths, reducing tire slip and friction. By keeping the tires at the optimal angle, this design improves stability and reduces tire wear, helping the robot make sharp turns without sliding or tipping.

# 3.0	Obstacle Management
In our project, we utilize the Clev3r-Python programming language to operate the robot. The programming structure is divided into two main sections: the Open Challenge and the Obstacle Challenge. This segment includes a flowchart and an overview of the code used for both challenges. Each part of the program is designed to meet specific requirements and optimize the robot's performance in different scenarios, providing a clear understanding of how the robot functions under distinct conditions.


## 3.1	Open Challenge
The left and right ultrasonic sensors help the robot determine its direction, whether it is moving clockwise or counterclockwise. These sensors detect the distance between the robot and nearby walls, allowing the robot to adjust its steering mechanism to avoid collisions. When an ultrasonic sensor reaches a certain threshold, indicating the absence of a wall, the robot will turn accordingly. Additionally, the gyro sensor ensures that the robot maintains a straight path and makes precise turns when necessary.
		

Below is the brief demostration video for Open Challenge
https://www.youtube.com/watch?v=1dNnKrStQGQ 
 
## 3.2 Obstacle Challenge
The upper Pixy 2 camera detects traffic signs. If it detects a red traffic sign, the robot's steering will turn right; if it detects a green traffic sign, the robot will respond similarly with the specified action for green. The bottom color sensor helps the robot follow the colored lines on the map. If it detects an orange line first, the robot will turn clockwise; if it detects a blue line first, it will turn counterclockwise.
The rear Pixy 2 camera assists with U-turn decisions. When it detects a red signal, the robot performs a U-turn; if it detects green, the robot continues completing three normal laps.
The gyro sensor maintains its primary role of ensuring the robot travels in a straight line and executes precise turns.


Below is the brief demostration video for Obstacle Challenge
https://www.youtube.com/watch?v=YTYfLjIolEA




