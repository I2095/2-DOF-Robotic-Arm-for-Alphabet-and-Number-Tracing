# 2-DOF-Robotic-Arm-for-Alphabet-and-Number-Tracing
A MATLAB/Simulink-based 2-DOF robotic arm that draws user-selected alphanumeric characters. UI retrieves character images, and converts them into vectorized paths stored in the MATLAB variable *simin*. Simulink uses these paths for inverse kinematics and motion control, enabling real-time, contact-free visualization and planar sketching.
# Overview
This project demonstrates how a simple 2-DOF robotic manipulator can be used to draw alphanumeric characters through automated trajectory generation. Users select a character through a MATLAB App Designer interface, after which the system extracts the character boundary, generates a drawing path, computes the required joint angles, and simulates the robotic arm motion in Simulink.

The project serves as an educational platform for understanding:

1. Robotic Manipulators
2. Inverse Kinematics
3. Image Processing
4. Trajectory Planning
5. Control Systems
6. MATLAB and Simulink Integration
## Project Workflow
### 1. User Input
The user selects an alphanumeric character through the MATLAB App Designer interface.
### 2. Image Processing
- Load character image
- Convert to grayscale
- Perform image inversion (if required)
- Binarize image
- Extract boundaries
### 3. Path Optimization
- Simplify contour points
- Remove redundant coordinates
- Preserve character shape
### 4. Trajectory Generation
- Normalize coordinates
- Scale trajectory to the robotic arm workspace
- Generate time vector
- Create `simin` matrix
### 5. Simulink Execution
- Pass `simin` to Simulink
- Compute inverse kinematics and generate joint trajectories
- Simulate robotic arm motion

### Technologies Used
-MATLAB
-Simulink
-MATLAB App Designer
-Image Processing Toolbox
-Robotics and Control System Concepts

# Output
The robotic arm traces the selected character in the simulation environment.

# UI for entering the number/letter
<img width="510" height="383" alt="image" src="https://github.com/user-attachments/assets/6300e9b5-4e37-46ce-81b1-6215ae6024e2" />

# Path traced by the robotic arm for various letters/numbers
# A
<img width="375" height="204" alt="image" src="https://github.com/user-attachments/assets/d3afea78-0af7-4b34-b36c-9ed2fdb61eb5" />
# 
# P
<img width="437" height="245" alt="image" src="https://github.com/user-attachments/assets/8126e7b9-2dc0-45f2-ae3a-5e1b1460e710" />

# 1
<img width="444" height="230" alt="image" src="https://github.com/user-attachments/assets/4c18df96-9cd6-4f47-907c-03032a79d1ea" />

# 4
<img width="452" height="254" alt="image" src="https://github.com/user-attachments/assets/83d37239-5a52-4be7-9e85-c0560cc93421" />

# 7
<img width="437" height="229" alt="image" src="https://github.com/user-attachments/assets/25cf19b2-a491-4151-bca0-d1364b4bc118" />

# Compare with handwritten to the path traced by robotic arm
<img width="334" height="212" alt="image" src="https://github.com/user-attachments/assets/3ee916b1-30c7-41a3-a63c-8def4c691e94" />
<img width="406" height="250" alt="image" src="https://github.com/user-attachments/assets/df7273c6-c89d-41d6-b4bd-258332d9fbb2" />
