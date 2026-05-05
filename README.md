#  Standalone Buck Converter PCB

![3D render of assembled PCB](/render.png)

A step-down (buck) converter PCB for **Triton Robotics**, designed to convert 24 V input to a regulated 5 V output. The board is laid out in EasyEDA and uses the AP63300WU-7 synchronous buck converter IC.

## Repository Contents

| File | Description |
|------|-------------|
| [buck.json](buck.json) | EasyEDA project file (schematic and PCB) |
| [Gerber_TR-AP63300-Standalone-Buck-Conv_PCB_TR-AP63300-Standalone-Buck.zip](Gerber_TR-AP63300-Standalone-Buck-Conv_PCB_TR-AP63300-Standalone-Buck.zip) | PCB Gerber files for fabrication |
| [BOM.csv](BOM.csv) | Bill of materials |
| [/render.png](/render.png) | 3D render of assembled board |
| [docs/C2158012.pdf](docs/C2158012.pdf) | AP63300WU-7 datasheet |

## Features

- **Input voltage:** 24 V (nominal)
- **Output voltage:** 5 V (regulated)
- **Connectors:** XT30 for power input and output
- **IC:** AP63300WU-7 synchronous buck converter
- **Design tool:** EasyEDA

## Hardware Overview

### IC: AP63300WU-7

The AP63300WU-7 is a synchronous buck converter with integrated power MOSFETs, suitable for point-of-load conversion from higher bus voltages (e.g. 24 V) down to 5 V. The feedback resistor divider on this board is chosen for **24 V → 5 V** operation.  

### Mounting

- **Screw size:** M2
- **Hole placement:** 5 mm from board edges

### Connectors

- **Power in / out:** XT30 connectors (input and output)

## Design Files

- Schematic and PCB are in the project’s EasyEDA design files.
- Feedback resistor values are set in the schematic for the 24 V → 5 V ratio; refer to the IC datasheet for the divider formula if changing output voltage.

## Usage Notes

- Ensure input polarity and voltage (24 V nominal) are correct before powering the board.
- Keep input/output traces and load connections within the current limits specified in the AP63300WU-7 datasheet.
- For production builds, verify mounting hole positions and clearances against Triton Robotics mechanical drawings.

## References

- [AP63300WU-7](https://www.diodes.com/part/view/AP63300) — manufacturer datasheet and application notes for feedback resistor selection and layout guidelines.

---
