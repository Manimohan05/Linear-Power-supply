# Linear Power Supply Design

## Abstract

This project, part of the EN2111 Electronic Circuit Design module at the University of Moratuwa, focuses on designing a linear power supply with a maximum current limit of 100 mA, incorporating over-current protection. The power supply delivers a stable output voltage adjustable from 8V to 14V, robust against fluctuating input voltages (16V to 20V) and varying load conditions. This repository contains the project files, including schematics, PCB designs, calculations, and documentation, developed by Group 19 under the supervision of Dr. Thusapparan Subramaniam.

## Introduction

A linear power supply provides a stable, precise output voltage, unlike unregulated power supplies that vary with load and input voltage fluctuations. By using a linear regulator, the power supply maintains a consistent output voltage (adjustable from 8V to 14V), reduces ripple and noise in the output direct current, and includes current limiting to protect against over-current damage. Key performance metrics include:
- **Line Regulation**: The ability to maintain the specified output voltage despite input voltage variations (16V to 20V).
- **Load Regulation**: The ability to maintain the specified output voltage under varying load conditions (e.g., resistors from 6Ω to 5000Ω).
- **Over-Current Protection**: Limits the output current to ~100 mA to safeguard the power supply and connected circuits.

The worst-case tolerance for output voltage stability is the sum of line and load regulation percentages. This project demonstrates the design, implementation, and testing of a linear power supply to meet these requirements.

## Project Objectives

- Design a linear power supply with an adjustable output voltage of 8V to 14V.
- Implement a current limit of 100 mA with over-current protection.
- Ensure output stability against input voltage fluctuations (16V to 20V) and varying load conditions.
- Prototype the circuit on a breadboard and finalize with a PCB design using EasyEDA.
- Document the design process, calculations, and performance results.

## Key Features

- **Voltage Regulation**: Utilizes a Zener diode and resistors to achieve stable output with minimal ripple and noise.
- **Current Limiting**: Targeted at 100 mA, achieved ~103 mA due to component tolerances.
- **Transistor**: TIP31C selected for power dissipation capacity exceeding 1.2W [(20V - 8V) × 100 mA].
- **PCB Design**: Designed with EasyEDA, adhering to rules such as 0.152 mm clearance, 0.254 mm copper width, and a 46 mm × 31 mm board.
- **Testing**: Validated for line and load regulation across input voltages (16V to 20V) and load conditions.

## Setup Instructions

### Prerequisites

- **Software**:
  - EasyEDA for viewing/editing schematic and PCB files.
  - A PDF reader for documentation.
  - A spreadsheet viewer (e.g., Microsoft Excel, LibreOffice Calc) for calculation files.
- **Hardware** (for replication):
  - TIP31C transistor.
  - Zener diode (refer to project documentation for selection details).
  - Resistors, capacitors, and other components as specified in the report.
  - Breadboard and jumper wires for prototyping.
  - PCB fabrication service for the final board.

### Steps to Replicate

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/<your-username>/Linear-Power-Supply.git
   cd Linear-Power-Supply
   ```

2. **Review Documentation**:
   - Open the project report PDF for details on calculations, schematics, and observations.
   - Refer to calculation files for input/output voltage ranges, Zener diode selection, and resistor values.

3. **Breadboard Implementation**:
   - Build the circuit on a breadboard using the schematic provided in the project files.
   - Test with input voltages from 16V to 20V, verifying output voltage (8V to 14V) and current limit (~100 mA).

4. **PCB Design**:
   - Open the EasyEDA schematic and PCB files.
   - Verify PCB design rules (e.g., 0.3 mm hole size, 46 mm × 31 mm board).
   - Use Gerber files for PCB fabrication.

5. **Testing**:
   - Test line regulation by setting the output to 8V and varying the input from 16V to 20V.
   - Test load regulation with resistors from 6Ω to 5000Ω.
   - Confirm current limitation at ~100 mA to ensure over-current protection.

## Observations

- **Output Voltage Range**: Achieved 6.8325V to 14.1534V, slightly wider than the target due to component tolerances.
- **Current Limitation**: Recorded at 103 mA, slightly above the 100 mA target.
- **Line Regulation**: Stable output (e.g., 8V) across input voltages from 16V to 20V, demonstrating effective regulation.
- **Load Regulation**: Consistent output voltage across load resistors from 6Ω to 5000Ω, as documented in the load variance table.

## Challenges

- **Component Selection**: Sourcing precise Zener diodes and resistors was challenging, leading to minor deviations in output.
- **Component Damage**: Improper connections during breadboard testing damaged some BC109 transistors.
- **Output Range**: Initial designs required iterative adjustments to achieve the target voltage range.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- **Supervisors**: Dr. Thusapparan Subramaniam.
- **Institution**: Department of Electronic & Telecommunication Engineering, University of Moratuwa.
- **Tools**: EasyEDA for PCB design, breadboard for prototyping.

For more details, refer to the project report in the repository. Contributions or feedback are welcome—please open an issue or submit a pull request!
