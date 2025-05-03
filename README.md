# CODE Fire Fighting - Intro to Robotics

This repository contains the project files and documentation for the **CODE Fire Fighting** course, part of the **Intro to Robotics** curriculum at KBTU.

## Project Overview

The goal of this project is to design and implement a robotic system capable of detecting and extinguishing fires in a controlled environment. This project introduces students to key concepts in robotics, including:

- Sensor integration
- Motor control
- Path planning
- Obstacle avoidance
- Fire detection and extinguishing mechanisms

## Repository Structure

This repository is divided into three main components:

1. **API**: A FastAPI-based application that uses the YOLOv8 model to detect fire and communicates via WebSocket protocol.
2. **Fire Detection Script**: A Python script utilizing the YOLOv8 model for fire detection.
3. **UGV Rover Code**: Code for the UGV (Unmanned Ground Vehicle) robot, specifically designed for the Raspberry Pi (ugv_rpi).

```
CODE-Fire-Fighting-Intro-to-Robotics/
├── api/                # FastAPI application for fire detection
├── model/     # Python script for YOLOv8-based fire detection
├── ugv_rpi/            # Code for the UGV rover
└── README.md           # Project overview and details
```

## Installation Instructions

### API (FastAPI Application)
1. Clone repository:
    ```bash
    git clone https://github.com/aminacoree/Robotics-Vision-Api.git
    cd Robotics-Vision-Api
    ```
2. Create a virtual environment and activate it:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4. Run the FastAPI application:
    ```bash
    uvicorn src.main:app --reload
    ```

### Fire Detection Script
1. Clone repository:
    ```bash
    git clone https://github.com/mkhmtolzhas/RoboticsVision.git
    cd RoboticsVision
    ```
2. Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the fire detection script:
    ```bash
    python main.py
    ```

### UGV Rover Code (Raspberry Pi)
1. Navigate to the `ugv_rpi` directory:
    ```bash
    cd CODE-Fire-Fighting-Intro-to-Robotics/ugv_rpi
    ```
2. Ensure the Raspberry Pi is set up with the necessary dependencies (refer to `docs/setup_rpi.md`).
3. Transfer the code to the Raspberry Pi using SCP or a similar method:
    ```bash
    scp -r . pi@<raspberry_pi_ip>:~/ugv_rpi
    ```
4. SSH into the Raspberry Pi:
    ```bash
    ssh pi@<raspberry_pi_ip>
    ```
5. Run the UGV rover code:
    ```bash
    python ugv_main.py
    ```


