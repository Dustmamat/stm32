# STM32 F401 Labs

This repository contains implementation of three laboratory sessions for Digital Systems Electronics using STM32 F401 microcontroller on NUCLEO board. Each lab explores different aspects of embedded programming from basic GPIO control to advanced interrupt handling.

## Hardware Requirements
- STM32 NUCLEO-F401RE board
- Oscilloscope
- Breadboard and jumper wires
- Potentiometer (10kΩ recommended)
- Resistors

## Development Environment
- STM32CubeIDE
- STM32Cube HAL/LL Libraries

## Lab Structure

### Lab 1 - LED Control and Square Wave Generation
**Original: LAB7 - Light Emitting Diode, Pushbutton and Square Waves**

Introduction to STM32 microcontroller programming with basic GPIO operations.

#### Projects:
- **Project 0**: Program example - Basic LED on/off (demonstration only)
- **Project 1.1**: LED control with pushbutton using low-level register manipulation
- **Project 1.2**: LED control with pushbutton using STM32Cube HAL/LL libraries
- **Project 1.3**: Variable frequency LED blinking controlled by pushbutton
- **Project 2**: Square wave generation (1 kHz) on GPIO pin D2 with multitasking simulation

**Learning Objectives:**
- Understanding STM32 GPIO configuration
- Register-level vs. HAL library programming approaches
- Basic timing loops and frequency control
- Introduction to multitasking concepts

---

### Lab 2 - Waveform Generation and ADC
**Original: LAB8 - Square Waveform Generation and Potentiometer**

Advanced timer usage for precise waveform generation and analog-to-digital conversion.

#### Projects:
- **Project 1.1**: 2 kHz square wave using TIM3 counter register polling
- **Project 1.2**: Square wave generation using Timer UIF flag polling (safer approach)
- **Project 1.3**: Dual square wave generation using Timer Output Compare (2.5 kHz and 12.5 kHz)
- **Project 1.4**: Automatic pin toggling with Timer Output Compare hardware feature
- **Project 1.5**: Variable frequency square wave (800 Hz - 4.5 kHz) controlled by potentiometer using ADC

**Learning Objectives:**
- Timer/Counter peripheral programming
- Output Compare functionality
- ADC configuration and polling
- Frequency calculation and mathematical operations
- Hardware vs. software pin control methods

---

### Lab 3 - Interrupt Programming
**Original: LAB9 - Interrupts**

Comprehensive interrupt handling for efficient multitasking and real-time applications.

#### Projects:
- **Project 1**: Interrupt-based variable frequency square wave generator with ADC
- **Project 2.1**: Three-interrupt system - 3-bit clock with different periods (1ms, 2ms, 4ms)
- **Project 2.2**: Four-interrupt system - Adding pushbutton interrupt for LED control
- **Project 2.3**: Five-interrupt system - Adding timer-triggered ADC for dynamic frequency control

**Learning Objectives:**
- Interrupt Service Routine (ISR) programming
- Multiple interrupt management and priorities
- Timer-triggered ADC conversions
- Real-time system design principles
- Interrupt vs. polling performance comparison

## Key Technical Concepts Covered

### Timer Configurations
- **Polling Methods**: Counter register polling vs. UIF flag polling
- **Output Compare**: Manual pin control vs. automatic hardware toggling
- **Interrupt Mode**: Timer interrupts for precise timing without CPU blocking

### ADC Implementation
- **Polling Mode**: Manual end-of-conversion checking
- **Single Conversion**: One-shot ADC measurements
- **Timer-Triggered**: Automatic periodic conversions

### Interrupt Management
- **Priority Levels**: Preemptive vs. non-preemptive interrupts
- **Multiple Sources**: Timer, ADC, and external interrupts
- **Real-time Constraints**: Jitter analysis and system stability

## Project Structure
```
├── Lab1_LED_Switch/
│   ├── Project_0_LED_Example/
│   ├── Project_1_1_LED_Switch_LowLevel/
│   ├── Project_1_2_LED_Switch_HAL/
│   ├── Project_1_3_Variable_Frequency/
│   └── Project_2_Square_Wave/
├── Lab2_Waveforms_ADC/
│   ├── Project_1_1_Counter_Polling/
│   ├── Project_1_2_UIF_Flag_Polling/
│   ├── Project_1_3_Output_Compare/
│   ├── Project_1_4_Auto_Toggle/
│   └── Project_1_5_Variable_Frequency/
└── Lab3_Interrupts/
    ├── Project_1_Interrupt_ADC/
    ├── Project_2_1_Three_Interrupts/
    ├── Project_2_2_Four_Interrupts/
    └── Project_2_3_Five_Interrupts/
```

## Reports
Detailed technical reports with implementation details, measurements, and analysis are available on Google Drive:
- [Lab 1 Report - LED Control and Square Waves](https://drive.google.com/file/d/1hsV5EYR_75NjKs9hn_be81x_258CKsiJ/view?usp=drive_link)
- [Lab 2 Report - Waveform Generation and ADC](https://drive.google.com/file/d/1L_643-ryyBo_g2ttcZ-6GXhYk5RjXppT/view?usp=drive_link)
- [Lab 3 Report - Interrupt Programming](https://drive.google.com/file/d/1TAyBV5u_wuT2i6h-Y3udHz81b1BI_-9C/view?usp=drive_link)

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/Dustmamat/stm32.git
   cd STM32-F401-Labs
   ```

2. **Open STM32CubeIDE**
   - Import existing projects from the cloned directory
   - Select the specific lab/project you want to work with

3. **Hardware Setup**
   - Connect STM32 NUCLEO-F401RE to your computer
   - For potentiometer projects: Connect potentiometer to analog input as shown in lab documents
   - Connect oscilloscope probes to designated output pins

4. **Build and Flash**
   - Compile the project in STM32CubeIDE
   - Flash to NUCLEO board
   - Use oscilloscope to verify waveform outputs

## Key Learning Outcomes

- **Embedded Systems Fundamentals**: Register manipulation, peripheral configuration, and hardware abstraction
- **Real-time Programming**: Interrupt handling, timing constraints, and multitasking
- **Signal Generation**: Timer-based waveform synthesis and frequency control
- **Analog Interface**: ADC programming
- **Debugging Techniques**: Oscilloscope measurements, debugger usage, and system verification
