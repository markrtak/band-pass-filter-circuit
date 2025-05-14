# Sallen Key Band Pass Filter Design and Implementation

## Description  
This repository contains the project report, simulation details, and hardware implementation for a *Sallen Key/Cascaded Band Pass Filter* designed as part of the ELCT 401: Electric Circuits II course. The project involved designing, simulating, and building a band-pass filter to meet specified frequency characteristics using the Sallen Key topology. Key deliverables include theoretical calculations, PSpice simulations, and oscilloscope results from the hardware prototype.  

---  

## Repository Contents  
- 📄 *sallen key report.pdf*: Full project report with design, simulations, and hardware results.  
- 📂 *circuit simulations.opj*: OrCAD Capture schematic for testing and running simulations.  
- 🖼️ *circuit schematic.png*: Schematic for the circuit.  
- 📝 *README.md*: This guide.  

---  

## Theoretical Background  
The Sallen Key band-pass filter is a cascaded active filter combining high-pass and low-pass stages. Key equations:  
- **Lower Cutoff Frequency**:  
  *fL = 1 / (2 * π * √2 * R1 * C1)*  
- **Higher Cutoff Frequency**:  
  *fH = 1 / (2 * π * √2 * R2 * C2)*  
- **Center Frequency**:  
  *f0 = √(fL * fH)*  

---  

## Filter Design  
### Component Values  
| Component | Value       |  
|-----------|-------------|  
| R1        | *1 kΩ*      |  
| R2        | *100 kΩ*    |  
| C1        | *10 nF*     |  
| C2        | *22 pF*     |  

### Calculated Frequencies  
- *fL = 11.25 kHz*  
- *fH = 51.15 kHz*  
- *f0 = 23.99 kHz*  

### Simulated Results (PSpice)  
- Lower cutoff (*f1*): *11.9 kHz*  
- Center frequency (*f0*): *24 kHz*  
- Upper cutoff (*f2*): *39 kHz*  

---  

## Simulation  
### Tools & Settings  
- **Software**: PSpice (OrCAD Capture).  
- **AC Sweep Profile**:  
  - Frequency Range: *100 Hz – 500 kHz* (Logarithmic).  
  - Input Signal: *1 V AC*.  
- **Time Domain Profile**:  
  - Input Signal: *Vsin* at *f < f0*, *f = f0*, *f > f0*.  
  - Run Time: *1 ms*.  

### Expected Outcomes  
- **AC Sweep**: Gain *vs.* frequency plot showing band-pass behavior.  
- **Time Domain**: Output voltage amplitude peaking at *f0*.  

---  

## Hardware Implementation  
### Components Used  
- Resistors: *3×1 kΩ*, *2×100 kΩ*.  
- Capacitors: *2×10 nF*, *3×22 pF*.  
- Op-Amps: *2×LM741*.  
- Breadboard, wires.  

### Key Steps  
1. Cascaded high-pass (HPF) and low-pass (LPF) stages on a breadboard.  
2. Validated output using an oscilloscope at *f = 11.9 kHz*, *24 kHz*, and *39 kHz*.  

---  

## Results  
### Simulation vs. Hardware  
| Parameter       | Calculated    | Simulated     | Hardware      |  
|-----------------|---------------|---------------|---------------|  
| Center Frequency | *23.99 kHz*   | *24 kHz*      | *24 kHz*      |  

### Oscilloscope Outputs  
- ***f < f0*** (*11.9 kHz*): Attenuated output.  
- ***f = f0*** (*24 kHz*): Maximum gain.  
- ***f > f0*** (*39 kHz*): Attenuated output.  

---  

## Getting Started  
### Running Simulations  
1. Open the PSpice project files in OrCAD Capture.  
2. Configure AC Sweep and Time Domain profiles as described in the report.  
3. Run simulations and compare results with *sallen key report.pdf*.  

### Replicating Hardware  
1. Purchase components listed in the report.  
2. Follow the breadboard layout from the report’s schematic.  
3. Test with a function generator and oscilloscope at three frequencies.  

---  

*This project is for academic purposes and does not require licensing.*  

---  
