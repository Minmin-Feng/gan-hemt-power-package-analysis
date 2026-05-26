# GaN HEMT Power Package Design and Analysis

This repository presents an academic electronic packaging project focused on the design and analysis of a custom power package for a 100 V GaN HEMT device targeting 48 V–12 V server power applications.

The project emphasizes low-parasitic package design, electrical simulation, thermal management, and experimental packaging evaluation. It was completed as part of an electronic packaging course project at Virginia Tech.

## Project Overview

Wide-bandgap GaN devices are increasingly used in high-frequency and high-current power conversion systems because of their low switching losses and high power density. However, fast switching also makes the package design critical, especially in terms of parasitic inductance, thermal resistance, and interconnect reliability.

In this project, a custom GaN HEMT package was designed and analyzed for a server power converter application. The work includes package geometry design, parasitic extraction, switching simulation, thermal resistance modeling, PCB thermal-via design, heatsink sizing, and experimental bonding reliability evaluation.

## Key Objectives

- Design a compact GaN HEMT power package suitable for 48 V–12 V server power conversion.
- Reduce power-loop and gate-loop parasitic inductance through package-level interconnect design.
- Evaluate switching behavior using extracted package parasitics.
- Develop a thermal management solution for high power density operation.
- Validate packaging process behavior through wire bonding, die attach, pull testing, and shear testing.

## My Main Contributions

- Developed package-level thermal analysis for the GaN HEMT power package.
- Calculated junction-to-case, PCB, and heatsink thermal resistance paths.
- Evaluated the dominant bottom-side cooling path through the die attach, thermal pad, PCB thermal vias, and heatsink.
- Verified the thermal solution under approximately 19.23 W device loss.
- Estimated the final junction temperature and thermal margin relative to the 150°C junction temperature limit.
- Supported system-level interpretation of electrical simulation and experimental packaging results.

## Technical Workflow

### 1. Package Design

The package was designed around a 100 V enhancement-mode GaN HEMT device. A clip-bonding interconnect structure was selected to reduce current path length, lower parasitic inductance, and improve electrical and thermal performance.

Key design considerations included:

- Low package inductance
- High-current conduction path
- Kelvin source connection
- Bottom-side thermal pad
- Copper clip interconnects
- Compact server power application footprint

### 2. Electrical Parasitic Extraction

ANSYS Q3D Extractor was used to extract package-level parasitic inductance and resistance. The extracted values were then incorporated into LTspice simulations to evaluate switching performance.

Key extracted results:

| Parameter | Value |
|---|---:|
| Power-loop inductance | 0.8313 nH |
| Gate-loop inductance | 0.9314 nH |
| Source resistance | 0.03569 mΩ |
| Drain resistance | 0.02747 mΩ |
| Gate resistance | 2.1797 mΩ |
| Kelvin-source resistance | 0.4956 mΩ |

### 3. LTspice Switching Simulation

The extracted Q3D parasitics were inserted into an LTspice buck converter simulation. The converter was configured for a 48 V input, 12 V output, 750 W load, and 200 kHz switching frequency.

The simulation was used to evaluate:

- Drain-source voltage overshoot
- Gate-source voltage overshoot
- Drain current ringing
- Switching loss
- Gate resistance optimization

A 7 Ω gate resistance was selected as a balanced design point because it suppressed positive gate-voltage overshoot while keeping device loss within the thermal design range.

### 4. Thermal Analysis

The thermal analysis focused on the bottom-side cooling path of the GaN HEMT package. A simplified thermal resistance network was developed from the junction to ambient.

The thermal path included:

1. GaN junction to bottom thermal pad  
2. Die attach layer  
3. PCB thermal-via region  
4. Bottom copper spreading area  
5. Aluminum heatsink  
6. Forced-air convection to ambient  

Key thermal results:

| Thermal / Power Result | Value |
|---|---:|
| High-side device loss | 19.23 W |
| PCB / heatsink pad-to-ambient resistance | 4.93 °C/W |
| Estimated junction-to-ambient resistance | 5.0 °C/W |
| Estimated junction temperature | 123°C |
| Maximum junction temperature limit | 150°C |
| Thermal margin | ~27°C |

The final design satisfies the thermal requirement and keeps the estimated junction temperature below the device limit.

### 5. Experimental Packaging Evaluation

Experimental evaluation was performed using standard packaging processes on DBC substrates.

The experimental work included:

- Wire bonding
- Die attach
- Pull testing
- Shear testing
- Failure mode observation

The wire-bond pull test results were used to evaluate bond strength and identify common failure modes such as heel break, wedge bond failure, and wire break.

## Tools and Skills Used

- ANSYS Q3D Extractor
- LTspice
- SolidWorks
- Thermal resistance modeling
- Power electronics packaging
- GaN HEMT package design
- PCB thermal-via design
- Heatsink design
- Wire bonding
- Die attach
- Pull testing and shear testing
- Technical documentation

## Repository Contents

| File | Description |
|---|---|
| `ECE5224_Final_Project_GitHub_Compressed.pdf` | Compressed final project report |
| `final project electrical simulation.zip` | Electrical simulation files and related project materials |

## Project Highlights

- Designed and analyzed a custom GaN HEMT power package for server power delivery.
- Achieved sub-1 nH extracted power-loop and gate-loop inductance.
- Integrated Q3D-extracted parasitics into LTspice switching simulation.
- Designed a bottom-side cooling solution using PCB thermal vias and an aluminum heatsink.
- Verified an estimated junction temperature of 123°C under 19.23 W device loss.
- Evaluated packaging process reliability through bonding and mechanical tests.

## Resume Summary

**Design and Analysis of a GaN HEMT Power Package | Virginia Tech University**

- Designed and analyzed a custom 100 V GaN HEMT power package for 48 V–12 V server power applications.
- Performed package-level parasitic extraction using ANSYS Q3D and integrated extracted values into LTspice switching simulations.
- Developed thermal resistance models for junction-to-case, PCB thermal vias, and heatsink cooling paths.
- Verified the bottom-side cooling design under 19.23 W device loss, achieving an estimated 123°C junction temperature with ~27°C margin below the 150°C limit.
- Supported experimental packaging evaluation including wire bonding, die attach, pull testing, and shear testing on DBC substrates.

## Note

This repository is intended as a technical portfolio summary of an academic electronic packaging project. It includes selected documentation, simulation files, and analysis results for professional and educational demonstration.
