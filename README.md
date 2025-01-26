# TESSERACT: Designing and Building Antenna Rotator for Satellite Tracking and Data Reception

TESSERACT (ITERA Tracker Radio Tracker Unit) is a project designed to enhance satellite communication by developing a system that tracks satellites and improves signal reception. It is equipped with a dual-axis antenna rotator, Arduino microcontroller, and a stepper motor-driven gearbox to accurately point antennas at satellite targets. The system supports communication with satellites like NOAA-19 and LAPAN A2 for enhanced signal reception during satellite contacts.

## Features

- **Dual-axis antenna rotator**: Capable of tracking satellites with precision.
- **Arduino-based control system**: Utilizes an Arduino Uno microcontroller for precise control and tracking.
- **Stepper motor drive**: Powered by a NEMA-17 stepper motor and a 60:1 geared gearbox for accurate movement.
- **SatNOGS integration**: Firmware developed by SatNOGS for satellite tracking and data reception.
- **SWR measurements**: SWR values of the antennas are tested to ensure signal efficiency.
- **Tracking tests**: Testing conducted on NOAA-19 and LAPAN A2 satellites to validate tracking and signal reception performance.

## Hardware Components

- **NEMA-17 Stepper Motor**: Drives the antenna rotator for precise positioning.
- **DRV8825 Motor Driver**: Controls the stepper motor for smooth movement.
- **Arduino Uno**: Acts as the central controller for motor drivers and sensors.
- **Infrared Sensors (FC-03)**: Used for determining home positions and preventing overshoot.
- **Yagi-Uda Antenna**: Used for UHF (433 MHz) and VHF (137 MHz) frequencies for satellite communication.
- **Gearbox**: A 60:1 worm gear assembly to increase torque and reduce motor speed.

## Software Components

- **SatNOGS Firmware**: Controls the antenna rotator and integrates with other tracking software.
- **Hamlib Interface**: Used for communication between the software and hardware for satellite tracking.
- **SatDump Software**: Provides tracking, controlling, and decoding capabilities for satellite signals.
- **SDRSharp**: Used for analyzing the signal-to-noise ratio (SNR) and recording audio signals.

## Setup and Installation

### Hardware Setup

1. **Assemble the Antenna Rotator**:
   - Install the NEMA-17 stepper motor with the gearbox assembly.
   - Attach the Yagi-Uda antennas to the rotator.
   - Connect the infrared sensors to the designated axes for home position detection.

2. **Connect to Arduino**:
   - Connect the Arduino Uno to the motor drivers, sensors, and power supply as described in the schematic.
   - Power the system using a 12V supply for both the Arduino and the motors.

3. **Mechanical Assembly**:
   - Mount the rotator and antennas to a stable structure that will support the tracking of satellites.

## Testing and Calibration
- SWR Calibration: Measure the SWR of the antennas using a NanoVNA analyzer to ensure proper impedance matching.
- Pointing Accuracy: Test the pointing accuracy by comparing the antenna's orientation with a digital compass.
- Slew Speed Testing: Measure the movement time for both azimuth and elevation axes to determine the slew speeds.

## Results and Performance
SWR Results:

- 137 MHz Yagi Antenna: SWR = 1.62
- 433 MHz Yagi Antenna: SWR = 1.81
Slew Speed:
- Average azimuth slew speed: 3.978°/s (clockwise)
- Average elevation slew speed: 3.598°/s (rising) and 3.618°/s (descending)
- Tracking Performance: The TESSERACT system successfully tracked NOAA-19 and LAPAN A2 satellites, improving signal consistency during satellite contact.

![Tesseract on Position](tesseractonpos.jpg)
