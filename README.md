# Gesture Driven Drone Simulator

## Project Overview
This project implements a real-time gesture controlled drone simulator using computer vision and human–machine interaction principles. Hand gestures captured through a webcam are interpreted using MediaPipe, translated into control commands, and applied to a simulated drone operating in a 3D-like virtual environment.

The system demonstrates how visual perception, gesture recognition, and decision logic can be integrated to control an intelligent system—an important concept in robotics and autonomous systems.

## 🧠 System Architecture
```text
Webcam Input
     ↓
Hand Landmark Detection (MediaPipe)
     ↓
Gesture Classification
     ↓
Temporal Smoothing (Stability Frames)
     ↓
Decision Logic
     ↓
Drone Motion Update
     ↓
3D Simulator Visualization
```

## ✋ Supported Gestures & Commands
```text
| Gesture                     | Meaning       | Drone Action         |
| --------------------------- | ------------- | -------------------- |
| ✊ Closed fist (Rock)        | LAND          | Drone lands          |
| ✋ Open palm (Paper)         | HOVER         | Drone holds position |
| ✌ Index + Middle (Scissors) | MOVE_FORWARD  | Drone moves forward  |
| ☝ Index finger              | MOVE_BACKWARD | Drone moves backward |
| ☝✌🖐 Three fingers          | MOVE_LEFT     | Drone moves left     |
```
To ensure reliability, gestures must remain stable across multiple frames before being applied.

## ▶️ How to Run the Project
### 1️⃣ Install Dependencies
```python
pip install -r requirements.txt
```
### 2️⃣ Run the Simulator
```python
python gesture-drone.py
```
### 3️⃣ Controls
- Perform hand gestures in front of the webcam
- Press q to quit the application

## 🔹Constraints
The drone’s movement is constrained within a defined radius, simulating physical world limits.
