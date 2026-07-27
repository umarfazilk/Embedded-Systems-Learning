<div align="center">

# 🚀 30 Days Embedded Systems Roadmap

## 📅 Day 01 — Microcontroller Fundamentals

*A structured journey to master Embedded Systems from the ground up.*

![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Day](https://img.shields.io/badge/Day-01-blue?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-Microcontroller-orange?style=for-the-badge)
![Language](https://img.shields.io/badge/Embedded-C-informational?style=for-the-badge)

---

*"The strongest firmware engineers don't memorize code—they understand hardware."*

</div>

---

# 📖 Table of Contents

- [🎯 Learning Objectives](#-learning-objectives)
- [📌 What is a Microcontroller?](#-1-what-is-a-microcontroller)
- [⚡ Microcontroller vs Microprocessor](#-2-microcontroller-vs-microprocessor)
- [🏗 Microcontroller Architecture](#-3-microcontroller-architecture)
- [🧠 CPU, ALU & Registers](#-4-cpu-alu--registers)
- [💾 Memory Types](#-5-memory-types)
- [🗺 Memory Map](#-6-memory-map)
- [⚙ Development Flow](#-7-development-flow)
- [📋 Interview Questions](#-interview-questions)
- [📝 Summary](#-summary)
- [📚 References](#-references)
- [➡ Next Topic](#-next-topic)

---

# 🎯 Learning Objectives

After completing today's learning, I should be able to:

- ✅ Explain what a Microcontroller is
- ✅ Differentiate MCU and MPU
- ✅ Understand MCU Architecture
- ✅ Explain CPU components
- ✅ Understand different Memory Types
- ✅ Read a Memory Map
- ✅ Explain the Embedded Development Flow

---

# 📌 1. What is a Microcontroller?

> **Definition**

A **Microcontroller (MCU)** is a compact computer integrated into a single Integrated Circuit (IC). It combines a processor, memory, and peripherals to perform dedicated control tasks efficiently.

Unlike a desktop processor, a microcontroller is designed for **real-time embedded applications** where low power consumption, reliability, and deterministic operation are essential.

---

## 📦 Internal Components

```text
                 Microcontroller
                       │
 ┌─────────────────────┼─────────────────────┐
 │                     │                     │
CPU                 Memory             Peripherals
 │               Flash / SRAM       GPIO UART SPI
 │                                     I²C ADC Timer
```

---

## 🌍 Real World Applications

| Application | Purpose |
|-------------|---------|
| Washing Machine | Motor Control |
| Smart Watch | Sensor Processing |
| Air Conditioner | Temperature Control |
| Drone | Flight Controller |
| Car ECU | Engine Control |
| IoT Devices | Data Collection |

---

> 💡 **Remember**

A Microcontroller is a **complete computer on one chip.**

---

# ⚡ 2. Microcontroller vs Microprocessor

| Feature | Microcontroller | Microprocessor |
|----------|----------------|---------------|
| CPU | ✅ | ✅ |
| Flash | Built-in | External |
| RAM | Built-in | External |
| GPIO | Built-in | External |
| Cost | Low | High |
| Power Consumption | Low | High |
| Applications | Embedded Systems | PCs & Servers |

---

## 📌 Quick Analogy

Think of a Microcontroller like a **Swiss Army Knife**.

Everything is inside one device.

A Microprocessor is like a **Desktop PC**.

You need external RAM, Storage, GPU and peripherals.

---

# 🏗 3. Microcontroller Architecture

```text
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

## 📖 Components

### 🧠 CPU

Executes Instructions.

---

### 💾 Flash

Stores Firmware.

---

### ⚡ SRAM

Stores Runtime Variables.

---

### 🔌 GPIO

Communicates with LEDs, Buttons and Sensors.

---

### ⏱ Timers

Generate Delays, PWM and Measure Time.

---

### 📡 UART / SPI / I²C

Communication Interfaces.

---

# 🧠 4. CPU, ALU & Registers

## CPU

The CPU continuously executes instructions stored inside Flash Memory.

Every instruction follows this cycle:

```text
Fetch
   │
Decode
   │
Execute
```

---

## ALU

The Arithmetic Logic Unit performs:

- Addition
- Subtraction
- Multiplication
- Comparison
- AND
- OR
- XOR

---

## Registers

Registers are tiny high-speed memories inside the CPU.

Examples:

- Program Counter (PC)
- Stack Pointer (SP)
- Status Register
- General Purpose Registers

---

# 💾 5. Memory Types

| Memory | Stores | Volatile | Speed |
|---------|--------|-----------|------|
| Flash | Firmware | ❌ | Medium |
| SRAM | Variables | ✅ | Very Fast |
| EEPROM | Settings | ❌ | Slow |
| ROM | Permanent Data | ❌ | Medium |
| DRAM | Computer Memory | ✅ | Fast |

---

## Memory Hierarchy

```text
Registers
    ↓
SRAM
    ↓
Flash
    ↓
External Storage
```

The closer the memory is to the CPU, the faster it is.

---

# 🗺 6. Memory Map

Every peripheral occupies a unique memory address.

Example:

```text
0x08000000  → Flash

0x20000000  → SRAM

0x40000000  → Peripherals
```

This concept is known as **Memory-Mapped I/O**.

Instead of talking directly to hardware, the CPU reads from and writes to memory addresses assigned to hardware registers.

---

# ⚙ 7. Development Flow

```text
Write Embedded C Code
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
     ELF / HEX / BIN
          │
          ▼
 Flash using ST-Link
          │
          ▼
 MCU Starts Executing
```

---

# 📋 Interview Questions

<details>

<summary>Click to View</summary>

### Beginner

- What is a Microcontroller?
- Difference between MCU and MPU?
- What is Flash Memory?
- What is SRAM?
- Why is SRAM Volatile?
- What is EEPROM?
- Explain Memory-Mapped I/O.
- What is a Register?
- Explain the Instruction Cycle.
- What is the Program Counter?

### Intermediate

- Why is Flash slower than SRAM?
- Why are Registers faster than SRAM?
- Explain Stack vs Heap.
- Why are peripherals mapped into memory?
- Explain the firmware compilation process.

</details>

---

# 📝 Summary

✅ MCU = CPU + Memory + Peripherals

✅ Flash stores Firmware

✅ SRAM stores Runtime Variables

✅ CPU executes Fetch → Decode → Execute

✅ Memory Map assigns addresses to Memories and Peripherals

✅ Embedded programs are converted into machine code before execution

---

# 📚 References

### Books

- 📖 *Making Embedded Systems* — Elecia White
- 📖 *The Definitive Guide to ARM Cortex-M3/M4* — Joseph Yiu
- 📖 *Embedded Systems: Introduction to ARM Cortex-M* — Jonathan Valvano

### Documentation

- STM32 Reference Manual
- STM32 Datasheet
- ARM Cortex-M Technical Reference Manual

---

# ➡ Next Topic

## 📅 Day 02 — GPIO (General Purpose Input Output)

We'll learn:

- Digital Inputs
- Digital Outputs
- Pull-Up & Pull-Down Resistors
- Push-Pull vs Open-Drain
- GPIO Registers
- LED Blinking
- Button Interfacing

---

<div align="center">

### ⭐ Day 01 Complete

*"A strong foundation is the first step toward mastering Embedded Systems."*

</div>