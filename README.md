# 📘 Multi-Agent Surveillance System

**👨‍💻 Authors:**
- **Sebastián Gerritsen Ortiz** - A01643364  
- **José Manuel Martínez Morales** - A01734279  
- **Rodrigo Castellanos Rodríguez** - A01643147  
- **Antoine Ganem Núñez** - A01644024 

**📅 Creation Date:** September 6, 2024  

## 📝 Project Description

This project presents a multi-agent surveillance system designed for construction zones. The system uses a combination of autonomous agents—drones, security personnel, and cameras—integrated with Unity and Python. YOLOv4 is utilized for object detection to identify intrusions and differentiate between workers and potential threats. 

### Key Features:
1. **DronAgent**: Autonomous patrol and random target selection. Capable of issuing alerts to security personnel when detecting anomalies.
2. **GuardiaAgent**: Centralized response agent for drone and camera alerts. Provides immediate directives to drones or on-ground security.
3. **CamaraAgent**: Static surveillance using YOLOv4 for detecting threats in real time.

## ⚙️ Functionalities

### 1. **DronAgent**
- **Setup**: Initializes position at (0,0), prepares interest points.
- **Random Patrol**: Selects random interest points to simulate dynamic surveillance patterns.
- **Alert Mechanism**: Sends real-time alerts to security personnel when threats are detected.

### 2. **GuardiaAgent**
- **Message Management**: Processes incoming alerts and issues directives to drones or on-ground teams.
- **Control Drones**: Provides specific navigation or operational commands to drones.

### 3. **CamaraAgent**
- **YOLOv4 Detection**: Analyzes images for potential intrusions with 76% accuracy.
- **Alerts**: Identifies and flags intrusions or threats to security personnel.

### **Agent Collaboration**  
Agents interact in a coordinated manner to ensure complete surveillance. Cameras handle static zones, while drones patrol dynamically, all under centralized supervision by the security agent.

## 🧪 Performance Metrics

1. **Simulation Success**: Achieved 87% success in 100 simulations by identifying and responding to anomalies effectively.
2. **YOLOv4 Precision**: Delivered 76% accuracy in distinguishing between workers and intruders over 200 test cases.

## 🚀 How to Run

### Installation Instructions:
1. Download the project files from [GitHub](https://github.com/Rodrigocr04/ConstruccionUnity).
2. Merge folders `SinAssets.zip` and `SoloAssets.zip` as described in the PDF instructions.

### Running the System:
1. Start the YOLO detection script:
   ```bash
   python deteccion_camara.py
Launch the agent system:
python agents.py
Open the Unity project in the Unity Editor and ensure all references are properly configured.
Unity Configuration:
Interest Points: Assign Unity objects (e.g., spheres) in the scene as "interest points" for the drones.
Zones: Place invisible Unity objects below key areas (e.g., doors) and tag them appropriately.
Camera References: Assign cameras to the scripts controlling object detection.
Inspector Configuration:
Reference points and tags in DronAgent.cs for patrol areas and drone spawn points.
Ensure proper connections between Unity scripts and Python server configurations (IPs and ports must match).
Tagging: Ensure tags for game objects match those expected in the scripts.
Notes:
deteccion_camara.py must run continuously. Restart it only if the Unity game restarts.
Update .cfg and .weights file paths in 4_yolo_opencv_detector.py if files are moved.
📚 References

GitHub Repository
Project Video
Training YOLO Model Guide
