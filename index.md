<p align="center">
  <img src="media/Render.png" alt="Atlas V3 Logo" width="700"/>
</p>

<h1 align="center">Atlas V3 ROS 2 Packages</h1>
<p align="center">
  <b>Modular, extensible, and modern ROS 2 packages for the Atlas V3 robotics platform.</b><br>
  <a href="https://github.com/machine0herald/ATLAS-ROS2-Packages">GitHub</a> •
  <a href="#install">Install</a> •
  <a href="#usage">Usage</a> •
  <a href="#contributing">Contributing</a>
</p>

---

## ✨ Overview

This directory contains the source code for the Atlas V3 ROS 2 packages. Each subfolder is a ROS 2 package providing specific functionality for the Atlas V3 robot platform.

---

## 📦 Directory Structure

```text
src/
├── atlas_v3/               # Core package (see README.txt inside)
├── atlas_v3_base/          # Motor control, calibration, and logging
├── atlas_v3_bringup/       # Launch files for bringing up the robot and subsystems
├── atlas_v3_camera/        # Camera drivers, publishers, and subscribers
├── atlas_v3_chess/         # Chess engine, agents, and move generation services
├── atlas_v3_demo/          # Demo nodes and launch files for MoveIt and ROS 2 control
├── atlas_v3_description/   # Robot URDF, meshes, and description files
├── atlas_v3_interfaces/    # Hardware interface definitions
├── atlas_v3_moveit_config/ # MoveIt configuration and launch files
├── atlas_v3_msgs/          # Custom ROS 2 message, service, and action definitions
├── atlas_v3_vision/        # Vision processing and perception nodes
└── ...
```

---

## 🚀 Notable Packages

| Package                  | Description                                                        |
|--------------------------|--------------------------------------------------------------------|
| **atlas_v3**             | Core package for Atlas V3 (see `atlas_v3/README.txt`).             |
| **atlas_v3_base**        | Motor control, calibration, joint state logging, PID logging.      |
| **atlas_v3_bringup**     | Launch files for robot, camera, chess, and all core systems.       |
| **atlas_v3_camera**      | Camera publishing/subscribing nodes using OpenCV and ROS 2.        |
| **atlas_v3_chess**       | Chess agents and ROS 2 service for move generation.                |
| **atlas_v3_demo**        | Demo nodes and launch files for MoveIt 2 and ROS 2 control APIs.   |
| **atlas_v3_description** | URDF, meshes, and robot description files.                         |
| **atlas_v3_interfaces**  | Hardware interface definitions for ROS 2 control.                  |
| **atlas_v3_moveit_config** | MoveIt configuration, planning pipelines, and launch files.      |
| **atlas_v3_msgs**        | Custom message, service, and action definitions.                   |
| **atlas_v3_vision**      | Vision and perception nodes for the Atlas platform.                |

---

## 🖼️ Screenshots & Media

<p align="center">
  <!-- Replace with your own images or GIFs -->
  <img src="media/atlas_demo.gif" alt="Atlas Demo" width="600"/>
  <br>
  <i>Atlas V3 in action: MoveIt planning, camera streaming, and chess agent.</i>
</p>

---

## ⚡ Install

**1. Update your system:**
```bash
sudo apt update && sudo apt upgrade
```

**2. Clone the repository into your ROS 2 workspace:**
```bash
git clone https://github.com/machine0herald/ATLAS-ROS2-Packages.git ~/atlas_v3_ws/src
```

**3. Install ROS 2 and system dependencies:**
```bash
cd ~/atlas_v3_ws
rosdep install --from-paths src --ignore-src -r -y
```

**4. (Optional) Install Python dependencies (recommended in a virtual environment):**
```bash
pip3 install chess torch opencv-python
```

**5. Build the workspace:**
```bash
colcon build
```

---

## 🛠️ Usage

**1. Source the workspace:**
```bash
source install/setup.bash
```

**2. Run a node (example: camera publisher):**
```bash
ros2 run atlas_v3_camera camera_publisher
```

**3. Launch the full robot stack (example):**
```bash
ros2 launch atlas_v3_bringup bringup.launch.py
```

---

## 🤝 Contributing

Pull requests, issues, and feature suggestions are welcome!  
Please see [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](../LICENSE) for details.

---

> **Note:** Each package contains its own README with more details about its functionality and usage.

<p align="center">
  <img src="https://raw.githubusercontent.com/machine0herald/ATLAS-ROS2-Packages/main/media/atlas_footer.png" alt="Atlas Footer" width="200"/>
</p>

