# Voice Controlled RGB Lighting System Using Silicon Labs SiWG917

## Project Overview

This project implements a voice-controlled RGB lighting system using the Silicon Labs SiWG917 Development Kit. The system utilizes the onboard microphone and a TensorFlow Lite for Microcontrollers based machine learning model to recognize predefined voice commands such as "ON" and "OFF".

Upon detecting a valid "ON" command, the onboard RGB LED turns on and cycles through different colors in sequence: Red, Green, Blue, and White. The "OFF" command turns off the currently active LED.

The project demonstrates the integration of embedded artificial intelligence, voice recognition, and RGB LED control on a low-power IoT platform while operating completely offline.

## Problem Statement

Traditional smart lighting systems often depend on mobile applications, cloud services, or external voice assistants for operation. These approaches increase system complexity, introduce internet dependency, and may affect responsiveness.

The objective of this project is to develop a standalone voice-controlled RGB lighting system capable of performing real-time voice recognition and LED control entirely on the device using embedded machine learning.

## Objectives

### Primary Objectives

* Implement offline voice recognition using TensorFlow Lite Micro.
* Detect predefined voice commands: ON and OFF.
* Control the onboard RGB LED using voice commands.
* Implement sequential color cycling for each ON command.
* Demonstrate embedded AI deployment on the Silicon Labs SiWG917 platform.

### Secondary Objectives

* Provide visual feedback through multiple RGB colors.
* Explore TinyML applications on embedded hardware.
* Establish a foundation for future smart lighting and automation systems.

## Hardware Used

* Silicon Labs SiWG917 Development Kit (BRD2605A)
* Onboard Microphone
* Onboard RGB LED
* USB Cable
* Development PC

## Software Used

* Simplicity Studio 6
* Visual Studio Code
* Silicon Labs SDK 2025.12.1
* TensorFlow Lite for Microcontrollers
* GCC ARM Toolchain
* CMake

## System Architecture

User Voice Command
↓
Onboard Microphone
↓
Audio Processing
↓
TensorFlow Lite Micro Model
↓
Command Recognition Engine
↓
ON / OFF Decision
↓
RGB LED Controller
↓
Color Selection Logic
↓
Onboard RGB LED

## Project Workflow

1. The onboard microphone continuously captures audio samples.
2. Audio data is preprocessed and converted into model features.
3. TensorFlow Lite Micro performs inference on the processed audio.
4. The command recognition engine determines whether the detected command is ON or OFF.
5. If the command is ON:

   * Increment the color index.
   * Select the next RGB color.
   * Turn the RGB LED ON.
6. If the command is OFF:

   * Turn the RGB LED OFF.
7. The system continues monitoring for additional voice commands.

## Color Cycling Logic

The RGB LED cycles through colors whenever a valid ON command is detected.

Sequence:

* ON #1 → Red

* OFF → LED Off

* ON #2 → Green

* OFF → LED Off

* ON #3 → Blue

* OFF → LED Off

* ON #4 → White

* OFF → LED Off

* ON #5 → Red

The sequence repeats cyclically.

## Machine Learning Model

The project uses a TensorFlow Lite for Microcontrollers keyword spotting model running locally on the SiWG917 device.

### Supported Commands

| Class | Command |
| ----- | ------- |
| 0     | ON      |
| 1     | OFF     |

The model performs all inference locally without requiring cloud connectivity or internet access.

## RGB LED Control

The onboard RGB LED is controlled using the Silicon Labs RGB LED driver.

### Color Values

| Color | RGB Value |
| ----- | --------- |
| Red   | 0xFF0000  |
| Green | 0x00FF00  |
| Blue  | 0x0000FF  |
| White | 0xFFFFFF  |

The LED color is updated whenever a new ON command is recognized.

## Testing and Verification

### Test 1

Voice Command: ON

Expected Result:

* RGB LED turns ON
* Color changes to next sequence color

### Test 2

Voice Command: OFF

Expected Result:

* RGB LED turns OFF

### Test 3

Multiple ON Commands

Expected Result:

* Sequential color cycling
* Red → Green → Blue → White → Red

All test cases were successfully verified.

## Results

The project successfully demonstrates:

* Voice Recognition
* Embedded AI Inference
* Real-Time Audio Processing
* RGB LED Control
* Sequential Color Cycling
* Offline TinyML Deployment

The system operates entirely on-device without requiring internet connectivity.

## Advantages

* Offline Operation
* Low Power Consumption
* Real-Time Response
* No Cloud Dependency
* User-Friendly Interaction
* Compact Implementation
* Demonstrates TinyML Deployment

## Applications

* Smart Lighting Systems
* Voice-Operated Switches
* Home Automation
* Assistive Technologies
* Human-Machine Interfaces
* Educational TinyML Demonstrations

## Future Enhancements

* Additional Voice Commands
* Brightness Control
* Voice-Controlled Appliances
* Mobile Application Integration
* Wi-Fi Dashboard
* BLE-Based Control
* Custom Voice Training

## Conclusion

A voice-controlled RGB lighting system was successfully implemented using the Silicon Labs SiWG917 Development Kit. The system accurately recognizes predefined ON and OFF voice commands and controls the onboard RGB LED accordingly. A sequential color cycling mechanism was implemented, allowing the LED to switch between Red, Green, Blue, and White on successive ON commands while turning OFF when the OFF command is detected. The project demonstrates the practical application of TinyML and embedded voice recognition for real-time smart device control on a low-power IoT platform.
