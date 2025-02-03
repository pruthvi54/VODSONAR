**VODSONAR: Visual-On-Demand-SOnar-Navigation-and-Recognition**

**Overview**

This repository implements an adaptive sonar activation strategy for an Autonomous Underwater Vehicle (AUV) using the DAVE simulator, which includes a Forward-Looking Sonar (FLS) module. The key idea is to optimize resource usage by activating the sonar only when necessary, based on camera detections.

**Problem Statement**

Sonar computations are computationally expensive and consume significant system resources. The goal of this project is to reduce unnecessary sonar usage and only enable it when required, improving efficiency while ensuring safe navigation.


**Video Demonstration in ROS-Gazebo**

https://github.com/user-attachments/assets/35a210b9-50d3-4bb3-93c3-8105185ee4b3


**Approach**

This algorithm follows a basic adaptive sensing strategy:

Straight-line navigation: The AUV moves forward without activating the sonar.

Camera-based detection: If the onboard camera detects an object, the sonar is activated.

Sonar distance estimation: The sonar determines the closest obstacle distance.

Camera-based decision-making: The camera helps determine the safest path, avoiding the danger zone distance.

Object tracking and surveying: Once an object of interest is found, the AUV maintains a safe, equal distance while keeping the object in its camera frame to complete the surveying phase.

**Implementation Details**

DAVE Simulator: Used for AUV and sonar simulations.

Camera Module: Detects objects and guides movement.

Sonar Module: Computes distances only when needed.

Navigation Logic: AUV avoids obstacles and maintains a survey distance.

**Future Enhancements**

Implement a more advanced decision-making model (e.g., deep learning-based perception).

Optimize sonar activation logic based on real-world testing.

Extend to multi-object tracking and path planning.
