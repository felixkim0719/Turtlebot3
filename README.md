# ROS TurtleBot3 Autonomous Driving Project

## Overview
This project implements autonomous driving using ROS and TurtleBot3. It incorporates line tracing, traffic light recognition, intersection recognition, barrier detection, and AI integration to allow the robot to navigate autonomously in various environments.
![](https://raw.githubusercontent.com/felixkim0719/Turtlebot3/main/ROS.jpg)
## Objective
The project aims to develop a robot capable of recognizing and responding to traffic signals, lines, and barriers, enabling autonomous navigation and task execution.

## Development Environment
- **OS**: Ubuntu 18.04 LTS
- **Platform**: ROS (ROBOTIS Packages)
- **Hardware**: TurtleBot3 Burger

## Key Technologies
### A. Line Tracing
- **Yellow Line Detection**: Detect and follow yellow lanes using HSV color space.
- **Center Coordinate Extraction**: Calculate lane center using OpenCV's `moments()` for path correction.
- **Control**: Use ROS Twist messages to adjust TurtleBot’s direction.

### B. Traffic Light Recognition
- **Color Filtering**: Convert image to HSV and filter for red and green lights.
- **Action**: Update mission status when a green light is detected.

### C. Intersection Recognition
- **Sign Detection**: Use DetectNet for intersection signs.
- **Hough Circle**: Detect circular objects for intersection signs and decide turns based on pixel analysis.

### D. Barrier Detection
- **Red Area Detection**: Identify and analyze barrier shapes using contour detection.
- **State Update**: Adjust TurtleBot’s state depending on whether the barrier is open or closed.

### E. AI Integration (DetectNet)
- **Object Detection**: Use DetectNet for real-time road sign and obstacle detection, integrated with ROS message passing.

### F. Core System
- **ROS Communication**: Use ROS Subscribers and Publishers to manage sensor data, driving commands, and mission statuses.
- **Mission Management**: Detect road conditions and update mission statuses accordingly.

## Conclusion
This project successfully demonstrates autonomous driving using ROS and TurtleBot3, with real-time image processing and AI technologies for environment recognition.
