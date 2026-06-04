# Voice Controlled Relay Light using Silicon Labs SiWG917

## Project Overview

This project demonstrates a voice-controlled home automation system developed using the Silicon Labs SiWG917 Development Kit. The system uses the onboard microphone and an embedded machine learning model to recognize predefined voice commands such as "ON" and "OFF". Based on the detected command, the system controls an external appliance through a relay module connected to GPIO_11.

The project showcases the practical implementation of Edge AI for real-time voice recognition and appliance control without requiring cloud connectivity, internet access, or external voice assistants. All processing is performed locally on the device, ensuring low latency, improved privacy, and reliable operation.

## Problem Statement

Conventional home automation systems often depend on mobile applications, cloud services, or third-party voice assistants. These approaches increase system complexity, introduce network dependency, and may affect response time.

The objective of this project is to develop a standalone voice-controlled automation system capable of local voice processing and real-time appliance control using embedded machine learning on the Silicon Labs SiWG917 platform.

## Objectives

### Primary Objectives
- Implement voice command recognition using an embedded AI model.
- Control external appliances using voice commands.
- Interface a relay module with the SiWG917 development board.
- Demonstrate real-time home automation functionality.

### Secondary Objectives
- Provide visual status indication using onboard LEDs.
- Explore embedded AI deployment on edge devices.
- Establish a foundation for future sensor and wireless integrations.

## Hardware Used

- Silicon Labs SiWG917 Development Kit (BRD2605A)
- Relay Module
- LED
- 330 Ω Resistor
- Jumper Wires
- Power Supply
- External Appliance / Bulb (for demonstration)

## Software Used

- Simplicity Studio 6
- Visual Studio Code
- Silicon Labs SDK 2025.12.1
- GCC ARM Toolchain
- CMake
- Simplicity Commander

## System Architecture

User Voice Command  
↓  
Onboard Microphone  
↓  
Embedded Machine Learning Model  
↓  
Command Recognition Engine  
↓  
GPIO_11 Control  
↓  
Relay Module  
↓  
Appliance / Light Bulb  

## Project Workflow

1. The user speaks a predefined command such as "ON" or "OFF".
2. The onboard microphone captures the audio signal.
3. The embedded TensorFlow Lite Micro model processes the audio.
4. The command recognition engine classifies the spoken command.
5. GPIO_11 is driven HIGH or LOW based on the detected command.
6. The relay module is activated or deactivated.
7. The connected appliance responds accordingly.

## GPIO Configuration

GPIO_11 is used as the output control pin for relay operation.

### ON Command

- GPIO_11 is set HIGH.
- Relay is energized.
- Appliance turns ON.

### OFF Command

- GPIO_11 is set LOW.
- Relay is de-energized.
- Appliance turns OFF.

## Testing and Verification

Prior to relay integration, GPIO operation was verified using an external LED connected through a current-limiting resistor.

### Test Cases

#### Test 1: Voice ON

Expected Result:
- LED ON
- Relay ON
- Appliance ON

#### Test 2: Voice OFF

Expected Result:
- LED OFF
- Relay OFF
- Appliance OFF

All test cases were successfully verified.

## Results

The project successfully demonstrates:

- Voice Recognition
- Embedded AI Inference
- Real-Time Command Processing
- GPIO-Based Device Control
- Relay Interface Integration
- Home Automation Functionality

The system performs all processing locally on the SiWG917 device and does not require internet connectivity.

## Advantages

- Offline Operation
- Low Latency Response
- Edge AI Processing
- Simple Hardware Architecture
- Expandable Design
- Low Power Consumption

## Applications

- Smart Homes
- Voice Controlled Lighting Systems
- Voice Controlled Appliances
- Assistive Automation
- Smart Classrooms
- Industrial Automation

## Future Enhancements

- Wi-Fi Based Dashboard Control
- BLE Mobile Application Control
- Multiple Relay Support
- Sensor Integration
- Additional Voice Commands
- Multi-Appliance Automation

## Conclusion

A voice-controlled home automation system was successfully developed using the Silicon Labs SiWG917 Development Kit. The project demonstrates the deployment of embedded machine learning for real-time voice recognition and appliance control. By processing commands locally and controlling external devices through GPIO and relay interfaces, the system provides an efficient, low-latency, and scalable solution for smart home and IoT applications.
