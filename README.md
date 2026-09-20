# ROS2 Flood Disaster Management Drone Simulation

A **ROS 2 and Gazebo-based drone simulation for disaster management and
flood-response scenarios**, integrating a custom drone model, sensor
simulation, 3D environment modelling, point-cloud mapping, visualization,
and manual drone control.

The project demonstrates how a simulated aerial robot can be used to explore
disaster-response scenarios where ground access may be restricted by
flooding, obstacles, or inaccessible terrain.

The drone was designed in **SolidWorks** and integrated into the ROS 2
simulation environment using **URDF**, with simulation and visualization
performed using **Gazebo and RViz**.

---

## Project Overview

Flooding and other natural disasters can make conventional ground-based
rescue and supply delivery difficult.

This project develops a simulated drone platform that can operate within a
virtual flood environment and demonstrates key robotic capabilities relevant
to disaster-response applications.

The simulation integrates:

- Custom drone CAD modelling
- SolidWorks-based drone design
- ROS 2
- Gazebo simulation
- URDF robot description
- RViz visualization
- IMU simulation
- GPS simulation
- Camera simulation
- Depth camera simulation
- LiDAR simulation
- 3D point-cloud generation
- Point Cloud Library (PCL)
- Flood-environment simulation
- Keyboard-based drone control
- Joystick-based drone control
- ROS 2 topic communication
- RQT graph visualization

---

## Project Objectives

The main objectives of the project were to:

- Design a simulated quadrotor drone for disaster-response applications.
- Develop the drone CAD model using SolidWorks.
- Convert the drone model into a ROS-compatible robot description.
- Simulate the drone in a virtual flood environment using Gazebo.
- Integrate multiple sensors for environmental perception.
- Visualize the drone and sensor data using RViz.
- Generate 3D point-cloud information using LiDAR/depth sensing.
- Explore 3D environmental mapping using the Point Cloud Library (PCL).
- Implement manual drone control using keyboard and joystick inputs.
- Study ROS 2 communication between the different control and simulation
  components.
- Demonstrate the potential use of aerial robots for disaster-management
  scenarios.

---

## Disaster Management Application

The simulation focuses on scenarios where flooding can make conventional
ground-based access difficult.

A drone can provide an aerial perspective of the affected environment and
can potentially support applications such as:

- Search and rescue
- Disaster-area reconnaissance
- Environmental mapping
- Obstacle detection
- Situational awareness
- Remote inspection
- Emergency-supply delivery
- Navigation through difficult or inaccessible terrain

This project is a **simulation and research prototype** intended to
demonstrate these concepts in a controlled virtual environment.

---

## System Architecture

The overall system combines the drone model, ROS 2 communication, Gazebo
simulation, sensors, visualization, mapping, and user control.

```text
                       ROS 2 DRONE SYSTEM
                              │
             ┌────────────────┼────────────────┐
             │                │                │
             ▼                ▼                ▼
        Drone Model       Sensor System     User Control
        (URDF/CAD)       IMU / GPS /       Keyboard /
             │            Camera / LiDAR     Joystick
             │                │                │
             └────────────────┼────────────────┘
                              │
                              ▼
                         ROS 2 Topics
                              │
                              ▼
                          Gazebo
                       Simulation
                              │
             ┌────────────────┼────────────────┐
             │                │                │
             ▼                ▼                ▼
            RViz          Point Cloud         RQT
        Visualization       / PCL           Graphs
                              │
                              ▼
                     3D Environment
                         Mapping
