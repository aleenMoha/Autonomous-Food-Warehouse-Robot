# 🤖 Autonomous Food Warehouse Robot

A project to automate the handling and management of a food warehouse using a robotic system without human intervention. The robot can navigate, identify, pick, place, and relocate items, while communicating with a central warehouse system.

---

## 📌 Step 1: Execution Algorithm

The robot operates based on the following logic:

### 🔁 Algorithm Overview:

1. **System Initialization**
   - Load warehouse data including: 
     - Item database
     - Number of rows and shelves
     - Current item locations
     - Orders queue
   - Allow modifications to this data in real-time (add, remove, update items).

2. **Warehouse Mapping**
   - Use a digital map (kroki) that contains the exact dimensions and structure of the warehouse.
   - Define routes for navigation and mark storage areas.

3. **Task Execution**
   - Receive tasks from the system:
     - Store new items
     - Retrieve items
     - Relocate existing items
   - Locate the item or a free slot using sensors and QR codes.
   - Navigate to the desired location and perform the action.

4. **System Update**
   - After every movement or placement, the robot updates the central system with:
     - New item location
     - Action confirmation
     - Task completion

5. **Loop**
   - Return to idle state and wait for the next task.

---

## ⚙️ Step 2: Robot Design

The robot has been designed with practical mobility, gripping, and vision systems to perform warehouse operations autonomously.

### 🤖 Mechanical Design:
- **Base:**  
  A circular platform with **four omni-directional wheels** for smooth 360° movement.

- **Arm:**  
  A robotic arm with **5 degrees of freedom (DOF)** for flexible vertical, horizontal, and rotational movement.

- **Gripper:**  
  A **4-finger gripper** for stable and accurate handling of various food packages.

- **Camera & QR Scanner:**  
  Located near the gripper to:
  - Identify objects using computer vision (AI)
  - Scan QR codes for inventory tracking
  - Guide the gripper with precise angle and positioning

- **AI & Vision System:**
  - Uses trained object detection (e.g., YOLO) to recognize items and calculate the best gripping point.
  - Handles image processing and detection in real-time.

- **Connectivity:**
  - Communicates with the central system using **Wi-Fi** to receive tasks and send updates.

---

## 📐 Step 3: Working Envelope

| Component          | Specification                   |
|-------------------|----------------------------------|
| Arm Reach          | 1.2 meters                       |
| Payload Capacity   | 5–10 kg                          |
| Base Rotation      | 360°                             |
| Joint Rotation     | ±180°                            |
| Operating Area     | 3 × 3 × 2 meters                 |
| Navigation Range   | Full mapped warehouse grid       |
| Precision          | ±1 cm in placement               |

---

## 🛠️ Step 4: Tinkercad Model

A simple prototype of the robotic arm is created on Tinkercad and can be accessed here:

🔗 [Tinkercad Link](https://www.tinkercad.com/things/6aWP76pGqVR-robotic-arm-with-5-dof?sharecode=2XcCnq44JPtY05GZjG0weN0cm4oA3UAmT7PBxmfz2Zs)

### Suggestions:
- Add a **circular base** using a cylinder shape.
- Place **4 wheels** equally spaced under the base.
- Attach a **small cube or cylinder** on the gripper as a camera.
- This model is conceptual and can be expanded into a full simulation or physical prototype.

---

## ✅ Summary

This project demonstrates a complete concept of a smart warehouse robot with:
- A detailed algorithm
- Efficient robot design
- Defined workspace
- Simple simulation model

The system is scalable and can be extended with real-time AI, SLAM navigation, and full warehouse automation systems.

---
