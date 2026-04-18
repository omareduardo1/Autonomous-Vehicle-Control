# Autonomous-Vehicle-Control
Fuzzy &amp; Neural Networks (MATLAB/Simulink)

📌 Project Overview
This repository showcases a university project focused on designing and implementing speed and steering control systems for an autonomous vehicle navigating a closed circuit. The environment consists of a 160x80m oval track where the vehicle must navigate efficiently without unnecessarily leaving its lane.
Note: The source code is no longer available; this repository serves as a portfolio piece presenting the final technical report, system architecture, and methodology.
🛠️ Tools & Technologies
•	MATLAB / Simulink
•	Fuzzy Logic Designer
•	Neural Network Toolbox / AnfisEdit
•	ROS (Robot Operating System) & STDR Simulator
🧠 System Architecture
1. Fuzzy Logic Controller (Mamdani)
I designed a Mamdani-type fuzzy controller to regulate both linear and angular velocities based on inputs from the vehicle's ultrasonic sensors.
•	Obstacle-Free Navigation: Implemented 5 fuzzy rules to keep the car centered and maintain a constant, optimal cruise speed of 35 km/h.
•	Obstacle Avoidance: Adjusted sensor ranges (up to 15m) and expanded the logic to 13 rules to handle evasive maneuvers, emergency braking, and lane tracking when encountering dynamic obstacles.
2. Neural Network Controller
To transition from fuzzy logic to machine learning, I generated my own dataset and trained a neural network:
•	Data Generation: I used the stable Fuzzy Controller to drive the simulated car for 3 complete laps, generating a dataset of approximately 2440 samples (sensor readings, velocities, and steering angles).
•	Feed-Forward Network: Trained a neural network using the extracted data to successfully replace the fuzzy controller in the obstacle-free scenario.
•	Neuro-Fuzzy (AnfisEdit) Attempt: For the obstacle course, I utilized MATLAB's AnfisEdit tool to handle the increased complexity. Although the dynamic environment proved too unstable for a perfect lap, this phase provided deep insights into the limitations of automated learning in unstructured environments.
📄 Documentation
For a deep dive into the membership functions, Simulink schematics, and training results, please refer to the attached PDF report.
