# Ambient Light Monitoring System Using Silicon Labs SiWG917 and VEML6035

## Project Overview

This project demonstrates ambient light monitoring using the onboard VEML6035 Ambient Light Sensor available on the Silicon Labs SiWG917 Development Kit. The system continuously measures surrounding light intensity and displays the measured lux value through the serial console.

The measured light intensity is classified into different brightness levels including Very Dark, Dim, Normal Room Light, and Bright. The project serves as a foundation for future smart lighting, energy-efficient automation, and sensor-based IoT applications.

The entire implementation runs locally on the SiWG917 platform without requiring external sensors, cloud connectivity, or additional processing units.

## Problem Statement

Many smart environments require continuous monitoring of ambient light conditions to improve energy efficiency, automate lighting systems, and enhance user comfort.

Traditional lighting systems operate independently of surrounding conditions, leading to unnecessary power consumption and reduced adaptability.

This project aims to implement a real-time ambient light monitoring system capable of measuring and classifying environmental brightness using the onboard VEML6035 sensor integrated with the Silicon Labs SiWG917 platform.

## Objectives

### Primary Objectives

* Interface and utilize the onboard VEML6035 Ambient Light Sensor.
* Measure ambient light intensity in lux.
* Display real-time sensor readings through the serial console.
* Classify environmental lighting conditions.

### Secondary Objectives

* Establish a foundation for automatic lighting control.
* Explore sensor integration on the SiWG917 platform.
* Demonstrate real-time environmental monitoring.
* Enable future IoT and smart building applications.

## Hardware Used

* Silicon Labs SiWG917 Development Kit (BRD2605A)
* Onboard VEML6035 Ambient Light Sensor
* USB Cable
* Development PC

## Software Used

* Simplicity Studio 6
* Visual Studio Code
* Silicon Labs SDK 2025.12.1
* GCC ARM Toolchain
* CMake
* Simplicity Commander
* Serial Terminal (PuTTY / TeraTerm)

## System Architecture

Ambient Light
↓
VEML6035 Sensor
↓
I2C Communication
↓
SiWG917 Processor
↓
Lux Calculation
↓
Brightness Classification
↓
VCOM Serial Output

## Project Workflow

1. The VEML6035 sensor continuously measures ambient light.
2. Light intensity data is transferred through the I2C interface.
3. The SiWG917 processes the sensor data.
4. Lux values are calculated and updated periodically.
5. The measured lux value is classified into predefined brightness categories.
6. Results are displayed through the VCOM serial terminal.
7. The system repeats the process continuously for real-time monitoring.

## Brightness Classification

The measured lux value is categorized into the following levels:

| Lux Range | Classification    |
| --------- | ----------------- |
| < 20      | Very Dark         |
| 20 – 80   | Dim               |
| 80 – 150  | Normal Room Light |
| > 150     | Bright            |

These thresholds can be modified depending on application requirements.

## Sensor Interface

The VEML6035 Ambient Light Sensor communicates with the SiWG917 using the I2C protocol.

### Features

* High sensitivity ambient light sensing
* Low power operation
* Wide dynamic range
* Accurate lux measurement
* Real-time monitoring capability

## Testing and Verification

### Test 1

Condition:
Sensor Fully Covered

Expected Result:

* Lux value decreases significantly
* Classification changes to Very Dark

### Test 2

Condition:
Normal Indoor Lighting

Expected Result:

* Moderate lux value
* Classification changes to Dim or Normal Room Light

### Test 3

Condition:
Direct Flashlight Illumination

Expected Result:

* High lux value
* Classification changes to Bright

All test cases were successfully verified.

## Results

The project successfully demonstrates:

* Ambient Light Measurement
* Real-Time Lux Monitoring
* Sensor Data Acquisition
* I2C Communication
* Environmental Brightness Classification
* Serial Console Visualization

The system accurately responds to changing environmental lighting conditions.

## Advantages

* Low Power Consumption
* Real-Time Monitoring
* Simple Hardware Architecture
* Accurate Light Measurement
* Easily Expandable
* Suitable for Smart Automation

## Applications

* Smart Lighting Systems
* Energy Management Systems
* Smart Buildings
* Home Automation
* Industrial Monitoring
* Environmental Sensing
* IoT Sensor Networks

## Future Enhancements

* Automatic Light Control using GPIO and Relay
* Smart Street Lighting Systems
* Wi-Fi Based Monitoring Dashboard
* Cloud Data Logging
* Mobile Application Integration
* Multi-Sensor Environmental Monitoring
* AI-Based Adaptive Lighting Control

## Conclusion

An ambient light monitoring system was successfully implemented using the onboard VEML6035 Ambient Light Sensor available on the Silicon Labs SiWG917 Development Kit. The project continuously measures ambient light intensity, calculates lux values, and classifies environmental brightness levels in real time. The implementation demonstrates effective sensor integration, I2C communication, and environmental monitoring capabilities while providing a scalable foundation for future smart lighting and IoT applications.
