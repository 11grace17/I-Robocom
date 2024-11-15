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
Our team is composed of three dedicated members who meticulously oversee the critical aspects of our autonomous vehicle's construction. Introducing Team I-Robocom from Malaysia - a passionate group devoted to refining the essential electromechanical components that power our fully autonomous vehicle. Let’s meet our team members: 

**Nelson Soo Hui Leng, Chang Pei Ru, and Grace Tan Hong Hui.**
![image](https://github.com/user-attachments/assets/84435c43-2075-4297-839f-361b506616f9)

# Performance video
This video provides an in-depth look at the structure of our self-driving car, a demonstration of its performance in both the Open Challenge and Obstacles Challenge, and a detailed explanation of how the car operates within each challenge. Please scan the QR code to watch the video and explore our project in action.
![image](https://github.com/user-attachments/assets/c58d3a75-2d0c-4547-bfa3-9f3a22b076c9)

# 1.0 Mobility management
This section provides an overview of the self-driving car’s design, detailing how its movement is controlled, along with the types of motors used and its implementation to the car. It includes a summary of the car’s chassis design and how various components are mounted on the structure. Additionally, key engineering principles such as speed, torque, and power are discussed.


## 1.1 Design of the self-driving car
The autonomous self-driving car is constructed using the Lego 45544 Mindstorms EV3 Education Set.
![image](https://github.com/user-attachments/assets/15e86b06-f310-496a-9d32-9d8f4bc5ba7e)

## 1.2  Chassis of the self-driving car
The design of the self-driving car’s chassis plays a crucial role in providing structural support, which ensures the car remains stable during fast movements like sharp turns and rapid accelerations. Therefore, our self-driving car is designed based on the concept of the right selection of the tyre, the implementation of motors, the implementation of differential gear and the engineering principle of the steering.

**(i) Selection of tyre**
We chose the LEGO 32019 rim and 86652 wheels because it provides a strong grip on different surfaces, reducing slipping and improving stability. It allows our self-driving car to move in a stable way while encountering both Open Challenge and Obstacle Challenge.

![image](https://github.com/user-attachments/assets/eac805de-df8d-4322-80ef-265ed60a7347)


**(ii) Implementation of motor and its engineering principle**
We use two EV3 Medium Motors to move the self-driving car forward and backwards. Placing them side by side horizontally or laterally to save space and make the car more compact. This setup also makes it easier to arrange the reduction gears and keeps the centre of gravity low, which improves stability during high-speed movement during the Open Challenge.

![image](https://github.com/user-attachments/assets/1f33b9f7-c5f6-473e-8bac-bc382e48809f)
The diagram below shows the details of the EV3 Medium Motor. 
![image](https://github.com/user-attachments/assets/46009c6d-7a98-416c-bd47-9d992a100104)
The EV3 Medium Motor is implemented due to its quick reactions and precise movements. As we can see from the diagram above, the running torque of 8Ncm and a stalled torque of 15 Ncm allow the self-driving car to handle the moderate forces that are needed for the steering, where small adjustments are needed. Moreover, the EV3 Medium Motor also provide us with a speed of 260 rpm, which means it can rotate quickly, making it ideal for rapid changes in direction or fine adjustments while avoiding traffic signs.

 **(iii) Implementation of differential gear**
The differential gear distributes power between two axles, allowing them to rotate at different speeds. This helps the self-driving car make smooth turns, especially when navigating corners of the inner walls.

![image](https://github.com/user-attachments/assets/e44b8791-7a6c-473c-b8a5-cfa9fa997d98)


**(iv) Engineering principle of steering**
Our self-driving car’s front steering uses a gear-down system, which slows down the turning motion for better control and precision in small rotations. This is helpful during making smooth and precise turns to avoid traffic signs.

![image](https://github.com/user-attachments/assets/fdee67cc-0364-4cfb-9363-5f409f2c4518)

We also use Ackermann steering geometry, which gives each front wheel a slightly different angle when turning. This setup allows the inner and outer tyres to follow separate paths, reducing tyre slip and friction. By keeping the tyres at the optimal angle, this design improves stability and reduces tyre wear, helping the robot make sharp turns without sliding or tipping.

![image](https://github.com/user-attachments/assets/88316739-27d2-447d-8ac8-3e3051477fa6)


## 1.3 Building of the self-driving car
In this section, the building instruction of the self-driving car and the video of the 3D printing parts process can be obtained through the QR Code below. 

![image](https://github.com/user-attachments/assets/a7b13b1a-1238-45a2-85c2-71374b74af31)

# 2.0	Power and sense management
This section will discuss the self-driving car’s power source and the sensors required to provide the car with information to negotiate the different challenges. The discussion included the reasons for selecting various sensors and how they are being used on the car together with power consumption. The Build of Materials (BOM) and wiring diagram are also provided.

## 2.1 Power source
We’ve boosted our self-driving car’s energy with the Soshine Rechargeable AA Lithium-ion Battery, providing 1.5V and 2600mWh of power to keep it running smoothly. This battery is the key source of energy for our robot.

![image](https://github.com/user-attachments/assets/5aed7002-80b5-4b2c-bb4d-ac39589a8e37)

## 2.2 Sensor
The self-driving car is equipped with a color sensor, two ultrasonic sensors, a gyro sensor and two Pixy 2 cameras. This powerful combination allows our self-driving car to encounter both Open and Obstacle Challenges. The diagram below shows the summary of the sensors that our self-driving car used.

![image](https://github.com/user-attachments/assets/b8dcb73a-8bbe-45a5-8e30-69a10eb230a5)

**(i) Pixy2 camera** 
Two Pixy2 cameras are used to assist our self-driving car. The Pixy2 camera will enable the self-driving car to identify multiple traffic signs at once while in motion. It will also be utilized for tasks like detecting walls and following lines on a map.

![image](https://github.com/user-attachments/assets/40a6704e-3554-4581-a4ae-95cfc640710e)

**(ii) Gyro sensor**
One gyro sensor is used to assist our self-driving car. The gyro sensor will help the self-driving car to calculate the angle and allow it to follow the correct orientation.

![image](https://github.com/user-attachments/assets/15cf901f-b041-475e-bc47-0d3e777293b1)

We initially used a compass sensor but switched to a gyro sensor due to interference from the self-driving car’s electromagnetic field, which affected compass accuracy. The LEGO EV3 gyro sensor effectively measures the self-driving car’s rotation angle, tracking tilt and rotational speed to maintain stable orientation and prevent drifting during turns. Although the EV3 gyro sensor can occasionally show an error on startup due to calibration issues, we had solved this issue by performing a hard reset each time the self-driving car is run, ensuring consistent accuracy in directional measurements.

**(iii) Ultrasonic sensor**
Two EV3 ultrasonic sensors are used to assist the self-driving car. The EV3 ultrasonic sensor is a digital device that measures the distance between the sensor and an object located in its path.

![image](https://github.com/user-attachments/assets/358e0880-a942-4073-b336-444ed6edfc69)

We originally used a Pixy2 camera to detect the walls, but due to frequent latency issues, we ended up switching to an ultrasonic sensor because it was able to read the required data faster and more directly. For both the open challenge and obstacle challenge, we chose to incorporate an ultrasonic sensor that measures the self-driving car’s distance from walls and detects corners. The sensor works by emitting sound waves and calculating the time it takes for them to return after hitting the wall. With this information, our self-driving car will be able to navigate effectively and make accurate turns, with the main goal of finishing the open challenge as quickly as possible.

**(iv) Color sensor**
One color sensor is only used in the obstacle challenge. It is used to determine when the self-driving car should turn. For a clockwise direction, the car will turn left every time it detects an orange line. Conversely, the robot will turn right when the color sensor detects a blue line in the counterclockwise direction. It works by measuring the intensity of the light that enters the sensor. The car uses the color sensor to determine whether the robot runs in a clockwise direction or counterclockwise direction by detecting the color line.

![image](https://github.com/user-attachments/assets/ce3f847f-f362-41e8-bbf7-e51e2a0f6cf3)

## 2.3 Build of materials
Below is the Build Of Material (BOM) that is used to build the self-driving car and ensure each component aligned together with the self-driving car's functional needs.





