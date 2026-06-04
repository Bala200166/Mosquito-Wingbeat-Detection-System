# Mosquito Wingbeat Detection System Using Optical Sensing

Prototype for mosquito wingbeat detection using a pulsed UV optical sensing approach, analog signal processing, and frequency-based event detection.

---

## Project Overview

Mosquitoes are vectors for diseases such as malaria, dengue fever, chikungunya, and Zika virus. This project investigates a low-cost optical sensing method for detecting mosquito wingbeat activity by measuring light interruptions caused by wing movement.

The objective was to validate the feasibility of detecting mosquito wingbeat frequencies using UV optical sensing, signal conditioning circuits, and digital pulse generation techniques.

---

## Key Objectives

- Develop an optical sensing system for mosquito wingbeat detection.
- Generate a pulsed UV light source for reliable measurements.
- Detect wingbeat-induced optical interruptions using a phototransistor.
- Design and simulate analog signal processing circuits.
- Convert weak sensor signals into clean digital pulses.
- Validate the concept through hardware proof-of-concept experiments.

---

## System Architecture

### Optical Detection Chain

UV LED Emitter  
→ Mosquito Wing Interruption  
→ Phototransistor Receiver  
→ Signal Conditioning Circuit  
→ Comparator with Hysteresis  
→ Digital Output

---

## Proof of Concept Development

### First Proof of Concept

A DC motor with a reflective element was used to simulate mosquito wing movement.

**Results**
- Successful optical event detection.
- Detectable pulse generation.
- Signal amplitude was relatively low.

### Second Proof of Concept

The optical arrangement was redesigned so the rotating element directly interrupted the UV light beam.

**Results**
- Improved pulse separation.
- Better signal quality.
- More realistic simulation of mosquito wing movement.

---

## Signal Processing Design

### Low-Pass Filter

**Purpose**
- Remove the 20 kHz UV carrier signal.
- Preserve mosquito wingbeat frequencies.

**Specifications**
- Cutoff frequency ≈ 1 kHz

### Inverting Amplifier

**Purpose**
- Amplify low-level phototransistor signals.
- Improve signal visibility for processing.

### High-Pass Filter

**Purpose**
- Remove DC offset.
- Improve signal quality.

**Specifications**
- Cutoff frequency ≈ 160 Hz

### Peak Hold Circuit

**Purpose**
- Extend pulse duration.
- Improve detection reliability.

### Comparator with Hysteresis (Schmitt Trigger)

**Purpose**
- Generate clean digital pulses.
- Improve noise immunity.

**Output**
- 0–5 V digital signal suitable for microcontroller inputs.

---

## UV LED Driver Circuit

A 555 Timer-based pulse generator was designed to drive the UV LED.

### Features

- 20 kHz pulse generation
- MOSFET-based switching stage
- Controlled duty cycle
- High optical pulse energy
- Safe LED operating conditions

### Validation Results

- Stable pulse generation achieved
- Approximately 40 mA RMS LED current
- Reliable operating conditions confirmed through simulation

---

## Experimental Results

### Observations

- Wingbeat-like events were successfully detected.
- Pulse spikes were clearly distinguishable from noise.
- Optical sensing approach was experimentally validated.
- Signal processing chain successfully generated digital output pulses.

### Conclusion

The proof-of-concept successfully demonstrated the feasibility of optical mosquito wingbeat detection using low-cost electronic components and analog signal processing techniques.

---

## Potential Applications

- Mosquito population monitoring
- Species behavior analysis
- Disease vector surveillance
- Environmental research
- Smart mosquito trap development

---

## Technologies Used

### Hardware

- UV LED
- Phototransistor
- NE555 Timer
- MOSFET Driver Circuit
- Operational Amplifiers
- Analog Signal Conditioning Circuits

### Software & Tools

- LTspice
- Oscilloscope Measurements
- Electronic Circuit Analysis

---

## Skills Demonstrated

- Analog Electronics Design
- Optical Sensing Systems
- Signal Processing
- Circuit Simulation
- Hardware Validation
- Experimental Testing
- Engineering Documentation
- Embedded Systems Fundamentals

---

## Future Improvements

- Real mosquito testing and data acquisition
- STM32-based signal processing platform
- Automatic species classification
- Wireless data transmission
- Autonomous field-deployable mosquito monitoring system

---

## Author

**SAKTHIVEL Balakumar**  
Master's Student (Bac+5) in Embedded Systems  
ISEP Paris, France
