# 🎮 Blueprints - Designing Basic Interactions

This project demonstrates basic gameplay interactions created using **Unreal Engine Blueprints**.  
The goal is to design simple yet functional interactions that respond dynamically to player input and actions.

---

## 🧩 Implemented Interactions

### 🚪 Door Opening Interaction
- **Description:** When the player approaches a door and presses the interact key (`E`), the door smoothly opens.
- **How it Works:**
  - A **Trigger Box** detects when the player enters its area.
  - Upon pressing `E`, a **Timeline** node animates the door rotation from closed to open.
  - The door closes automatically when the player exits the trigger area.

---

### 💡 Light Activation Interaction
- **Description:** The player activates a light when entering a trigger area.
- **How it Works:**
  - A **Trigger Box** surrounds the area where the player enters.
  - When the player overlaps the trigger, a **Toggle Visibility** (or **Set Light Enabled**) node switches the light on.
  - When the player leaves, the light turns off again.

---

### 🪙 Coin Collection Interaction
- **Description:** The player can collect coins scattered in the level.
- **How it Works:**
  - Each coin has a **Collision Sphere** that detects player overlap.
  - On overlap, the coin is destroyed using a **Destroy Actor** node.
  - The player’s score variable increments by +1.
  - A simple **UI Widget** can optionally display the updated score.

---

## 🧠 Key Concepts Used
- Blueprint Classes  
- Trigger Boxes and Collisions  
- Event Graphs (BeginOverlap, EndOverlap)  
- Timeline Animations  
- Variables and Branch Logic  
- Player Input Binding  

---

## 🧪 Testing
Each interaction was tested to ensure:
- Proper response to player input (`E` for interaction).  
- Correct overlap detection for coins and triggers.  
- Smooth and error-free transitions (e.g., door animation timing).
