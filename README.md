# SignalScope
# UNDER CONSTRUCTION
## Overview
Hello traveler! Signal Scope is a project focused on building a motorized tracking antenna system designed to receive and decode images from weather satellites. The system combines mechanical steering with control algorithms to maintain a strong signal lock on satellites as they move across the sky, enabling the reception of high-quality Earth images from NOAA and METEOR M2 satellites. This is an ongoing project, and I'll update my progress here as I continue.


## Features
**Motorized Antenna Tracking:** The system uses a motorized mount to physically steer the antenna, ensuring it follows the satellite's path for continuous signal reception.

**Control Algorithm:** Implemented to precisely control the antenna's movement, optimizing signal strength and accuracy.

**Software-Defined Radio (SDR):** Integrates with an SDR to receive and record signal.

**Satellite Image Decoding:** Utilizes WXtoIMG to convert received signals into real-time weather images.

## Components
### Antenna
The antenna is a directional yagi assembly, responsible for capturing the signals from weather satellites. This antenna is tuned for receiving signals in the 137 MHz range, which is used by NOAA weather satellites. The choice of using a Yagi antenna was made to effectivley utilize the motorized mount. A directional antenna, like a Yagi, will have significantly more gain than an omnidirectional antenna, but must be pointed at the signal source.
### Gimbal (Motorized Mount)
The gimbal is a motorized mount that allows the antenna to track satellites as they move across the sky. It provides precise control over the antenna's azimuth and elevation, enabling continuous alignment with the satellite. It consists of a frame which is belt driven by an azimuth stepper motor, and an elevation stepper motor (again, belt driven). The gimbal is controlled by an arduino microcontroller, which receives real-time positional commands from a Raspberry Pi. The Pi is responsible for calculating the orbital dynamics of a tracked satellite and implementing inverse kinematics to convert to positional commands for the gimbal.
### Control Algorithm
The control algorithm utilizes control principles to steer the antenna. The raspberry pi calculates the satellite's position based on orbital pass data, then sends control signals to the gimbal's motors to keep the antenna aligned with the satellite throughout its pass. The algorithm ensures smooth tracking and minimizes signal loss.

## Research

## Build & Lessons Learned

## Getting Started (If you *really* want to replicate this project)
### Prerequisites

A motorized antenna mount

Software-Defined Radio (SDR) (e.g., RTL-SDR)

Yagi Antenna

Microcontroller/FPGA for control algorithms

Satellite tracking software (e.g. n2yo.com)

WXtoIMG for decoding weather satellite images

### Installation

Clone the repository:

git clone https://github.com/yourusername/SatTrack-Antenna.git



Set up the hardware components and connect them to your microcontroller.

Install necessary software for SDR and satellite image decoding.

### Usage
Find pass parameters from n2yo.com (start azimuth, end azimuth, max elevation, start/end time)

Run the control algorithm on the raspberry pi to start tracking the satellite.

Use the SDR to receive signals as the antenna tracks the satellite.

Decode the received signals to obtain weather images.

## Thanks!
Be curious on your journey!
