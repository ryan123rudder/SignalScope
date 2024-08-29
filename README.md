# SignalScope
# **UNDER CONSTRUCTION**
## Overview
Hello Traveler! Signal Scope is a project focused on building a motorized tracking antenna system designed to receive and decode images from weather satellites. The system combines mechanical steering with advanced control algorithms to maintain a strong signal lock on satellites as they move across the sky, enabling the reception of high-quality weather data.

## Features
Motorized Antenna Tracking: The system uses a motorized mount to physically steer the antenna, ensuring it follows the satellite's path for continuous signal reception.
Guidance, Navigation, and Control (GNC) Algorithms: Implemented to precisely control the antenna's movement, optimizing signal strength and accuracy.
Software-Defined Radio (SDR): Integrates with an SDR to decode satellite signals into usable data, including weather images.
Low-Noise Amplifier (LNA): Enhances weak signals received from satellites for clearer data reception.
Satellite Image Decoding: Utilizes software to convert received signals into real-time weather images.

## Components
### Antenna
The antenna is the core of the system, responsible for capturing signals from weather satellites. This project uses a Yagi-Uda or helical antenna, both of which are well-suited for receiving signals in the 137 MHz range, commonly used by NOAA weather satellites. The antenna is carefully tuned and positioned to maximize signal strength and clarity.
### Gimbal (Motorized Mount)
The gimbal is a motorized mount that allows the antenna to track satellites as they move across the sky. It provides precise control over the antenna's azimuth and elevation, enabling continuous alignment with the satellite. The gimbal is controlled by a microcontroller or FPGA, which receives real-time data about the satellite's position and adjusts the antenna's orientation accordingly.
### Electronics
The electronics system includes the microcontroller or FPGA, a Low-Noise Amplifier (LNA), and the Software-Defined Radio (SDR). The microcontroller/FPGA is responsible for executing the control algorithms and managing the gimbal's movements. The LNA boosts the weak signals received from satellites, ensuring they are strong enough for processing. The SDR acts as the receiver, converting the radio signals into digital data that can be decoded into weather images.
### Control Algorithm
The control algorithm is the brain of the system, using Guidance, Navigation, and Control (GNC) principles to steer the antenna. It calculates the satellite's position based on orbital data and adjusts the gimbal's motors to keep the antenna aligned with the satellite throughout its pass. The algorithm ensures smooth tracking, minimizes signal loss, and compensates for factors like wind or mechanical imperfections.

##Getting Started
###Prerequisites

A motorized antenna mount
    Software-Defined Radio (SDR) (e.g., RTL-SDR)
    Compatible antenna (Yagi-Uda or helical)
    Microcontroller/FPGA for control algorithms
    Satellite tracking software (e.g., WXtoIMG for decoding weather satellite images)

###Installation

Clone the repository:

 bash

git clone https://github.com/yourusername/SatTrack-Antenna.git

Set up the hardware components and connect them to your microcontroller/FPGA.
    Install necessary software for SDR and satellite image decoding.

###Usage

Run the control algorithm to start tracking the satellite.
    Use the SDR to receive signals as the antenna tracks the satellite.
    Decode the received signals to obtain weather images.

Acknowledgments

Special thanks to the open-source community for providing tools and resources that made this project possible.
