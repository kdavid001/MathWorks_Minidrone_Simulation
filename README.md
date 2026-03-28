# 🚁 MathWorks Minidrone Autonomous Flight Controller

![Minidrone Simulation Demo](link-to-your-gif-or-image-here.gif)
*A simulation of the autonomous line-following and waypoint navigation logic.*

## Overview
This repository contains the perception and control algorithms developed for the **MathWorks Minidrone Competition**. The objective of this project was to design an autonomous flight controller capable of guiding a quadcopter through a track using strictly downward-facing camera feeds and onboard sensor data. 

The core focus of this build was transitioning from raw algorithmic logic into formal simulation environments, bridging computer vision with classical control theory.

## 🛠️ Tech Stack & Tools
* **Environment:** MATLAB & Simulink
* **Logic & State Management:** Stateflow
* **Perception Engine:** Computer Vision Toolbox (Image Processing, Line Detection)
* **Control Systems:** PID Controller Tuning

## System Architecture
The autonomous pipeline is divided into three primary subsystems:

### 1. Perception (Vision Processing)
The drone relies on a downward-facing camera to process the track. 
* Applied [insert your image processing technique, e.g., color thresholding/edge detection] to isolate the track path.
* Calculated the centroid and angular offset of the path relative to the drone's current body frame to generate error signals.

### 2. Planning (Stateflow Logic)
State machines were utilized to govern the high-level behavior of the quadcopter.
* **Takeoff State:** Stabilizing altitude to [insert meters] before initializing vision algorithms.
* **Tracking State:** Continuously updating heading and velocity commands based on the perception error signals.
* **Landing State:** Detecting the end-of-track marker and executing a safe descent protocol.

### 3. Control (Flight Dynamics)
Translating the path-planning logic into physical motor commands.
* Tuned the PID controllers for pitch, roll, and yaw to minimize overshoot when navigating sharp turns.
* [Optional: Mention any specific noise filtering or sensor fusion you applied to the altitude/IMU data].

## How to Run the Simulation
1. Clone this repository to your local machine.
2. Ensure you have **MATLAB** installed with the **Simulink Support Package for PARROT Minidrones**.
3. Double-click the `[Your_Project_Name].mlproj` file. This will automatically configure the MATLAB paths and load the necessary workspace variables.
4. Open the main `.slx` model and execute the simulation.

## Results & Key Takeaways
* **Performance:** The algorithm successfully navigated the track in [Insert Time] without losing the path lock.
* **Bottlenecks Addressed:** [Insert one cool engineering problem you solved, e.g., "Initially struggled with the drone over-correcting on sharp corners, but resolved this by dampening the derivative gain on the yaw controller."]

---
*Built by Team Logos*
