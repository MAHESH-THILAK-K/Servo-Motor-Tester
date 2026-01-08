# Servo Motor Tester

**A compact 555 timer-based servo tester with adjustable pulse width control for hobby servo testing and calibration.**

## 🔧 Project Overview
A standalone servo tester that generates standard hobby servo PWM signals (50 Hz, 1-2 ms pulses) using an NE555 timer IC configured as an astable multivibrator. A 100kΩ potentiometer provides smooth position control from minimum to maximum servo travel.

**Key goals of this design:**
- Simple analog PWM generation (no microcontroller required)
- Standard 3-pin servo output interface
- Compact, hand-solderable 2-layer PCB
- Visual power/activity indication
- Precise pulse width control via potentiometer

## 📌 Key Features

**Power Input**
- 6V DC via 2-pin header (J1)

**Servo Output** 
- Standard 3-pin header (J2) - VCC/GND/SIG
- Compatible with all hobby servos

**Pulse Control**
- 100kΩ potentiometer (RV1) for 1-2ms pulse width
- Real-time servo position adjustment

**Timing Network**
- R2 (3.3MΩ), R3 (56kΩ), D2 (1N4148)
- C1 (22nF) timing capacitor
- Diode-separated charge/discharge paths

**Status Indication**
- Power LED (D1) with 1kΩ current limiting

## 📂 Repository Structure

```
SERVO-MOTOR-TESTER/
│
├── README.md              # Project documentation
├── LICENSE                # CC-BY-SA-4.0 license
├── Hardware/              # KiCad source files
│   ├── Servo-Motor-Tester.kicad_pro
│   ├── Servo-Motor-Tester.kicad_sch
│   └── Servo-Motor-Tester.kicad_pcb
├── Gerber/                # Manufacturing files
├── 3D MODELS/             # STEP files
├── BOM FILES/             # Bill of materials
└── Images/                # PCB renders & schematics
```

## 🛠️ Hardware Overview

**Core Components**

U1: NE555 Timer (DIP-8) - PWM generation
RV1: 100kΩ Potentiometer - Pulse width control  
C1: 22nF - Timing capacitor
R1: 1kΩ - LED current limit
R2: 3.3MΩ, R3: 56kΩ - Timing resistors
D1: LED - Power indicator
D2: 1N4148 - Charge/discharge diode


**Connectors**

J1 (2-pin): VCC (6V), GND - Power input
J2 (3-pin): GND, VCC, SIG - Servo output


**Mechanical**
- Four M2 mounting holes
- Compact ~35×25mm PCB
- Clear silkscreen labeling

## 🔌 Connections


Power Input (J1):
Pin 1 ── VCC (6V DC)
Pin 2 ── GND

Servo Output (J2):  
Pin 1 ── GND
Pin 2 ── VCC (6V)
Pin 3 ── SIG (PWM)


## 🏭 Manufacturing

The Gerber files include:
- Top/Bottom copper layers
- Solder mask & silkscreen
- Drill files & board outline
- Ready for JLCPCB, PCBWay, or any PCB fab

**PCB Specs:**
- 2-layer, 1.6mm thickness
- Hand-solderable SMD + THT mix

## 🚀 Build Instructions

1. Solder SMD resistors (R1, R2, R3 - 0805)
2. Install 555 timer (DIP-8 socket recommended)  
3. Solder THT components (C1, D1, D2, RV1)
4. Mount headers (J1, J2)
5. Power with 6V DC supply
6. Connect servo to J2
7. Adjust RV1 for servo position control

## 📄 Firmware
**No firmware required** - Pure analog 555 timer design

## 📸Diagrams
Board renders, schematics, and assembly photos available in:
- `Hardware/` - KiCad source files
- `Images/` - Visual documentation

## 📜 License
**CC-BY-SA-4.0** - Free to use, modify, and share with attribution.

## 🙌 Contributions
Contributions, improvements, and documentation updates welcome. Open issues or pull requests.

## 📧 Contact
For questions or collaboration, open an Issue or contact **Thilak**.
