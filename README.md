# ADAS Model-Based Design Project

## 📌 Project Overview
This project implements an **Advanced Driver Assistance System (ADAS)** using **Model-Based Design (MBD)** in MATLAB/Simulink. It follows the **V-Model Development** approach, integrating model-based simulation, Software-in-the-Loop (SIL), and Hardware-in-the-Loop (HIL) testing to validate system performance.

## 📂 Project Structure
```
ADAS_MBD_Project/
├── Vehicle_Direction_Detector/
│   ├── Steering_Direction_Detection.slx
│   ├── Speed_Control.slx
│   ├── Lane_Keeping.slx
│   ├── Collision_Avoidance.slx
│   ├── Test_Harness/
│   │   ├── SIL_Model.slx
│   │   ├── HIL_Setup.slx
│   │   ├── Simulation_Tests.m
│   └── README.md
└── Docs/
    ├── System_Requirements.pdf
    ├── Design_Specifications.pdf
    ├── Test_Cases.xlsx
```

## 🚗 Features Implemented
- **Steering Direction Detection** ✅
- **Speed Control** ✅
- **Lane Keeping Assistance** ✅
- **Collision Avoidance System** ✅
- **Software-in-the-Loop (SIL) Testing** ⚙️
- **Hardware-in-the-Loop (HIL) Integration** ⚙️

## 🛠️ Setup & Installation
### **1. Prerequisites**
- MATLAB (Recommended: R2023b or later)
- Simulink
- MinGW-w64 Compiler / Microsoft Visual Studio C++ Compiler
- MATLAB Embedded Coder (For SIL & HIL Testing)

### **2. Configure MATLAB Compilers**
Ensure MATLAB detects the compiler:
```matlab
mex -setup C++
```
If MinGW-w64 is missing, install it via:
```matlab
matlab.addons.install('MinGW Support Package')
```

### **3. Run the Simulink Model**
1. Open MATLAB.
2. Navigate to `ADAS_MBD_Project/Vehicle_Direction_Detector/`
3. Run `Steering_Direction_Detection.slx`

### **4. Test SIL Model**
1. Open `Test_Harness/SIL_Model.slx`
2. Click **Run** to simulate the system.

## 🧪 Testing & Validation
| Test Case | Description | Status |
|-----------|------------|--------|
| TC-01 | Steering angle detection (>30° right, <-120° left) | ✅ Passed |
| TC-02 | Speed Control at varying accelerations | ✅ Passed |
| TC-03 | Lane keeping response to road curves | ✅ Passed |
| TC-04 | Obstacle detection & collision avoidance | ✅ Passed |

## 📌 Troubleshooting
**Error:** `Supported compiler not found`
- Ensure MinGW-w64 or Microsoft Visual Studio C++ is installed.
- Manually set compiler path:
```matlab
setenv('MW_MINGW64_LOC', 'C:\ProgramData\MATLAB\SupportPackages\mingw_w64')
```
- Restart MATLAB and run:
```matlab
mex -setup C++
```

## 📞 Contact
For any queries or contributions, feel free to reach out:
📧 Email: ahmedmohsen-209@hotmail.com
💼 LinkedIn: (https://linkedin.com/in/ahmed-mohsen-abouelyazed)

