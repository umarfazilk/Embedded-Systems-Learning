<div align="center">

# 🚀 Day 01 — Microcontroller Fundamentals

### 📘 Topic: Introduction to Microcontrollers and Embedded Systems

*Building the foundation for Embedded Systems and Firmware Development.*

![Day](https://img.shields.io/badge/Day-01-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Difficulty](https://img.shields.io/badge/Difficulty-Beginner-green?style=for-the-badge)
![Category](https://img.shields.io/badge/Category-Embedded%20Systems-orange?style=for-the-badge)

---

*"Every embedded system starts with understanding the hardware that runs the software."*

</div>

---

# 📖 Overview

Welcome to **Day 01** of my Embedded Systems Learning Journey.

Today's objective was to understand the **building blocks of every embedded system**—the **Microcontroller**.

Instead of jumping directly into programming, I focused on understanding how a microcontroller is organized internally, how memory is structured, and how firmware eventually executes on hardware.

By mastering these fundamentals first, future topics such as GPIO, Timers, UART, SPI, I²C, ADC, Interrupts, and RTOS become much easier to understand.

---

# 🎯 Learning Objectives

After completing Day 01, I can:

- ✅ Explain what a Microcontroller is
- ✅ Differentiate between MCU and MPU
- ✅ Understand the internal architecture of an MCU
- ✅ Explain CPU, ALU and Registers
- ✅ Understand Flash, SRAM, EEPROM and ROM
- ✅ Read a basic Memory Map
- ✅ Explain the Embedded Firmware Development Flow

---

# 📚 Topics Covered

- What is a Microcontroller?
- Microcontroller vs Microprocessor
- Internal Architecture
- CPU, ALU and Registers
- Memory Types
- Memory Map
- Firmware Development Flow

---

# 📌 What is a Microcontroller?

A **Microcontroller (MCU)** is a compact computer integrated into a single Integrated Circuit (IC).

It combines:

- CPU
- Flash Memory
- SRAM
- GPIO
- Timers
- Communication Interfaces
- Analog Peripherals

Unlike a computer processor, a microcontroller is designed for performing a **specific task repeatedly** while consuming very little power.

---

# 🏗 Internal Architecture

```
                     +----------------+
                     |      CPU       |
                     +--------+-------+
                              |
              +---------------+---------------+
              |                               |
        +-----+------+                 +------+------+
        | Flash ROM |                 |    SRAM      |
        +------------+                 +-------------+
              |
      +-------+-------------------------------+
      | GPIO | Timer | ADC | UART | SPI | I2C |
      +----------------------------------------+
```

---

# ⚡ MCU vs MPU

| Feature | Microcontroller | Microprocessor |
|----------|----------------|---------------|
| CPU | ✅ | ✅ |
| RAM | Internal | External |
| Flash | Internal | External |
| GPIO | Internal | External |
| Cost | Low | High |
| Power | Low | High |
| Applications | Embedded Systems | Computers |

---

# 🧠 CPU, ALU & Registers

## CPU

The CPU executes every instruction stored inside Flash memory.

---

## ALU

Responsible for

- Addition
- Subtraction
- Comparison
- Logical Operations

---

## Registers

Registers are the fastest memory inside the processor.

Examples:

- Program Counter (PC)
- Stack Pointer (SP)
- General Purpose Registers
- Status Register

---

## Instruction Cycle

```
Fetch
   ↓
Decode
   ↓
Execute
```

This process repeats continuously while the microcontroller is powered.

---

# 💾 Memory Types

| Memory | Purpose | Volatile |
|---------|---------|-----------|
| Flash | Stores Firmware | ❌ |
| SRAM | Variables | ✅ |
| EEPROM | Configuration | ❌ |
| ROM | Permanent Data | ❌ |
| DRAM | Computer RAM | ✅ |

---

# 🗺 Memory Map

Example:

```
0x08000000  → Flash

0x20000000  → SRAM

0x40000000  → Peripherals
```

The CPU communicates with peripherals by accessing these memory addresses.

This technique is called **Memory-Mapped I/O**.

---

# ⚙ Firmware Development Flow

```
Embedded C Code
        │
        ▼
Preprocessor
        │
        ▼
Compiler
        │
        ▼
Assembler
        │
        ▼
Linker
        │
        ▼
HEX / BIN File
        │
        ▼
Flash to MCU
        │
        ▼
Program Executes
```

---

# 🌍 Real World Applications

Microcontrollers are found in:

- Washing Machines
- Smart Watches
- Air Conditioners
- Automotive ECUs
- IoT Devices
- Medical Equipment
- Industrial Automation
- Drones
- Robotics

---

# 💡 Key Takeaways

- A Microcontroller is a complete computer on one chip.
- Flash stores firmware permanently.
- SRAM stores runtime variables.
- Registers are the fastest memory inside the CPU.
- Firmware executes using the Fetch → Decode → Execute cycle.
- Hardware peripherals are controlled using Memory-Mapped I/O.

---

# 📋 Interview Questions

### Basic

- What is a Microcontroller?
- Difference between MCU and MPU?
- What is Flash Memory?
- What is SRAM?
- Explain Memory-Mapped I/O.
- What is EEPROM?
- Explain Registers.
- What is the Program Counter?

### Intermediate

- Why is SRAM faster than Flash?
- Explain the firmware compilation process.
- Explain Stack and Heap.
- Why are peripherals memory mapped?

---

# 📊 Visual Summary

The complete visual summary for today's learning is available below.

```
Reference/
└── microcontroller-fundamentals-overview.png
```

> Open the image for a quick revision of all concepts covered in Day 01.

---

# 📚 References

## Books

- Making Embedded Systems — Elecia White
- The Definitive Guide to ARM Cortex-M Processors — Joseph Yiu
- Embedded Systems: Introduction to ARM Cortex-M Microcontrollers — Jonathan Valvano

## Documentation

- STM32 Reference Manual
- STM32 Datasheet
- ARM Cortex-M Technical Reference Manual

---

# 🎯 Day 01 Status

| Topic | Status |
|--------|:------:|
| Theory | ✅ |
| Architecture | ✅ |
| Memory | ✅ |
| Development Flow | ✅ |
| Revision Image | ✅ |

---

# ➡ Next Topic

**Day 02 — GPIO (General Purpose Input/Output)**

Topics to Learn:

- GPIO Registers
- Input Mode
- Output Mode
- Pull-up & Pull-down
- Push-Pull vs Open-Drain
- LED Blinking
- Button Interfacing

---

<div align="center">

## ⭐ Day 01 Completed Successfully

*"Strong embedded engineers build strong fundamentals before writing firmware."*

</div>
