# Sallen Key Band Pass Filter Design and Implementation

## Description
This repository contains the project report, simulation details, and hardware implementation for a **Sallen Key/Cascaded Band Pass Filter** designed as part of the ELCT 401: Electric Circuits II course. The project involved designing, simulating, and building a band-pass filter to meet specified frequency characteristics using the Sallen Key topology. Key deliverables include theoretical calculations, PSpice simulations, and oscilloscope results from the hardware prototype.

---

## Repository Contents
- 📄 `sallen key report.pdf`: Full project report with design, simulations, and hardware results.
- 📂 `Simulation Files` (if available): PSpice schematic and simulation profiles.
- 📷 `Hardware Results`: Oscilloscope screenshots for input/output voltages at three frequencies.
- 📝 `README.md`: This guide.

---

## Theoretical Background
The Sallen Key band-pass filter is a cascaded active filter combining high-pass and low-pass stages. Key equations:  
- **Lower Cutoff Frequency**:  
  \( f_L = \frac{1}{2\pi\sqrt{2} R_1 C_1} \)  
- **Higher Cutoff Frequency**:  
  \( f_H = \frac{1}{2\pi\sqrt{2} R_2 C_2} \)  
- **Center Frequency**:  
  \( f_0 = \sqrt{f_L \cdot f_H} \)  

---

## Filter Design
### Component Values
| Component | Value       |
|-----------|-------------|
| R1        | 1 kΩ        |
| R2        | 100 kΩ      |
| C1        | 10 nF       |
| C2        | 22 pF       |

### Calculated Frequencies
- \( f_L = 11.25 \, \text{kHz} \)
- \( f_H = 51.15 \, \text{kHz} \)
- \( f_0 = 23.99 \, \text{kHz} \)

### Simulated Results (PSpice)
- Lower cutoff (\( f_1 \)): 11.9 kHz  
- Center frequency (\( f_0 \)): 24 kHz  
- Upper cutoff (\( f_2 \)): 39 kHz  

---

## Simulation
### Tools & Settings
- **Software**: PSpice (OrCAD Capture).  
- **AC Sweep Profile**:  
  - Frequency Range: 100 Hz – 100 kHz (Logarithmic).  
  - Input Signal: 1 V AC.  
- **Time Domain Profile**:  
  - Input Signal: Vsin at \( f < f_0 \), \( f = f_0 \), \( f > f_0 \).  
  - Run Time: 100 ms.  

### Expected Outcomes
- **AC Sweep**: Gain vs. frequency plot showing band-pass behavior.  
- **Time Domain**: Output voltage amplitude peaking at \( f_0 \).  

---

## Hardware Implementation
### Components Used
- Resistors: 3×1 kΩ, 2×100 kΩ.  
- Capacitors: 2×10 nF, 3×22 pF.  
- Op-Amps: 2×LM741.  
- Breadboard, wires, and power supply (±12 V).  

### Key Steps
1. Cascaded high-pass (HPF) and low-pass (LPF) stages on a breadboard.  
2. Validated output using an oscilloscope at \( f = 11.9 \, \text{kHz} \), \( 24 \, \text{kHz} \), and \( 39 \, \text{kHz} \).  

---

## Results
### Simulation vs. Hardware
| Parameter       | Calculated | Simulated | Hardware |
|-----------------|------------|-----------|----------|
| Center Frequency | 23.99 kHz  | 24 kHz    | ~24 kHz  |

### Oscilloscope Outputs
- **\( f < f_0 \)** (11.9 kHz): Attenuated output.  
- **\( f = f_0 \)** (24 kHz): Maximum gain.  
- **\( f > f_0 \)** (39 kHz): Attenuated output.  

---

## Getting Started
### Running Simulations
1. Open the PSpice project files in OrCAD Capture.  
2. Configure AC Sweep and Time Domain profiles as described in the report.  
3. Run simulations and compare results with `sallen key report.pdf`.  

### Replicating Hardware
1. Purchase components listed in the report.  
2. Follow the breadboard layout from the report’s schematic.  
3. Test with a function generator and oscilloscope at three frequencies.  

---

## Contributors
- **Mark Raymond Takla**  
- Team members (if applicable): [Add names here]  

---

## License
This project is for academic purposes and does not require licensing.  

--- 

🛠 For questions or issues, please open a **GitHub Issue**.  
