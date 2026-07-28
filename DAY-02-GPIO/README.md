<div align="center">

# 🚀 Day 02 — GPIO (General Purpose Input / Output)

### *The Pins That Bring Microcontrollers to Life* 🔌

![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Day](https://img.shields.io/badge/Day-02-blue?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-GPIO-orange?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-STM32%20%7C%20Arduino%20%7C%20ESP32-informational?style=for-the-badge)

*"A microcontroller without GPIO is like a brain without hands."*

---

## 📈 Learning Progress

```text
Day 01 ✅ Microcontroller Fundamentals
      │
      ▼
Day 02 ✅ GPIO
      │
      ▼
Day 03 ⏳ Binary Numbers & Bitwise Operations
```

</div>

---

# 📖 Overview

GPIO (**General Purpose Input/Output**) is one of the most important peripherals inside every microcontroller.

It acts as the communication bridge between the **CPU** and the **outside world**.

Without GPIO, a microcontroller can execute millions of instructions but cannot interact with LEDs, buttons, sensors, motors, displays, or communication devices.

---

# 🎯 Learning Objectives

After completing Day 2, I can:

- ✅ Explain what GPIO is
- ✅ Differentiate Input and Output pins
- ✅ Understand Logic HIGH & Logic LOW
- ✅ Explain Active HIGH & Active LOW
- ✅ Understand Floating Inputs
- ✅ Explain Pull-up & Pull-down Resistors
- ✅ Differentiate Push-Pull and Open-Drain Outputs
- ✅ Understand GPIO Registers
- ✅ Explain 3.3V vs 5V Logic Levels
- ✅ Follow GPIO Best Practices

---

# 🛣️ GPIO Roadmap

```text
Microcontroller
      │
      ▼
GPIO
 ├── Input
 ├── Output
 ├── Logic Levels
 ├── Pull-up / Pull-down
 ├── Output Drivers
 ├── Registers
 └── Protection
```

---

# 🧠 What is GPIO?

GPIO stands for **General Purpose Input/Output**.

It is a programmable pin on a microcontroller that allows it to communicate with external hardware.

### Input

Reads signals from the outside world.

Examples:

- Push Button
- Motion Sensor
- Switch
- IR Sensor

### Output

Controls external devices.

Examples:

- LED
- Relay
- Buzzer
- Motor Driver

---

# 🔄 GPIO Data Flow

## Input Mode

```text
Button
   │
   ▼
GPIO Pin
   │
   ▼
GPIO Register
   │
   ▼
CPU
```

---

## Output Mode

```text
CPU
 │
 ▼
GPIO Register
 │
 ▼
GPIO Pin
 │
 ▼
LED
```

---

# ⚡ Logic HIGH & Logic LOW

Digital electronics understands only two states.

| Logic | Binary | Voltage |
|--------|---------|----------|
| LOW | 0 | 0V |
| HIGH | 1 | 3.3V / 5V |

> HIGH voltage depends on the microcontroller.

STM32 → 3.3V

Arduino UNO → 5V

ESP32 → 3.3V

---

# 🔴 Active HIGH vs Active LOW

## Active HIGH

```text
HIGH → Device ON

LOW → Device OFF
```

Example

```text
GPIO HIGH

↓

LED ON
```

---

## Active LOW

```text
LOW → Device ON

HIGH → Device OFF
```

Example

```text
GPIO LOW

↓

LED ON
```

Many STM32 development boards use **Active LOW LEDs**.

---

# 🌊 Floating Inputs

A GPIO input pin left unconnected is called a **Floating Input**.

```text
GPIO

│

Nothing Connected

↓

Random HIGH

Random LOW

Random HIGH
```

A floating input behaves like a small antenna and picks up electrical noise.

This causes unpredictable readings.

---

# ⬆️ Pull-up Resistor

A pull-up resistor connects the GPIO pin to VCC.

```text
3.3V

│

10kΩ

│

GPIO

│

Button

│

GND
```

Default State

```text
HIGH
```

Button Pressed

```text
LOW
```

---

# ⬇️ Pull-down Resistor

A pull-down resistor connects the GPIO pin to Ground.

```text
GPIO

│

10kΩ

│

GND

│

Button

│

3.3V
```

Default State

```text
LOW
```

Button Pressed

```text
HIGH
```

---

# 🔌 Push-Pull vs Open-Drain

| Feature | Push-Pull | Open-Drain |
|----------|-----------|------------|
| HIGH Output | Yes | External Pull-up Required |
| LOW Output | Yes | Yes |
| Speed | High | Medium |
| Used For | LEDs, Motors | I²C Bus |

---

# 🏗️ GPIO Registers

A microcontroller controls GPIO through registers.

```text
CPU

↓

GPIO Registers

↓

GPIO Pin
```

Important Registers

| Register | Purpose |
|-----------|----------|
| MODER | Pin Mode |
| IDR | Input Data Register |
| ODR | Output Data Register |
| BSRR | Set/Reset Output |
| PUPDR | Pull-up/Pull-down |

---

# ⚡ 3.3V vs 5V Logic

| MCU | Logic HIGH |
|------|------------|
| STM32 | 3.3V |
| ESP32 | 3.3V |
| Arduino UNO | 5V |

⚠️ Never connect a 5V signal directly to a non-5V-tolerant STM32 GPIO.

---

# 💻 Simple Embedded C Example

```c
// LED Output

pinMode(LED_BUILTIN, OUTPUT);

digitalWrite(LED_BUILTIN, HIGH);
```

```c
// Button Input

pinMode(BUTTON, INPUT_PULLUP);

int state = digitalRead(BUTTON);
```

---

# 🏭 Real World Applications

| Device | GPIO Usage |
|----------|------------|
| LED | Output |
| Push Button | Input |
| Relay | Output |
| Temperature Sensor | Input |
| LCD Display | Output |
| Servo Motor | PWM Output |
| PIR Sensor | Input |
| Smart Lock | Input & Output |

---

# 💡 Best Practices

- ✔ Never leave GPIO inputs floating.
- ✔ Use Pull-up or Pull-down resistors.
- ✔ Check voltage compatibility before connecting peripherals.
- ✔ Configure GPIO mode before use.
- ✔ Never exceed the maximum GPIO current rating.
- ✔ Read the datasheet before connecting external hardware.

---

# 🎯 Practice Completed

- ✅ Blinked an LED using GPIO
- ✅ Read a Push Button
- ✅ Understood GPIO Input/Output
- ✅ Learned Logic Levels
- ✅ Explored Pull-up & Pull-down Concepts

---

# 📋 Quick Revision

```text
GPIO

↓

Input

↓

Output

↓

HIGH / LOW

↓

Active HIGH / LOW

↓

Floating Input

↓

Pull-up

↓

Pull-down

↓

Push-Pull

↓

Open-Drain

↓

GPIO Registers

↓

3.3V vs 5V

↓

Best Practices
```

---

# 🧠 Interview Questions

### Beginner

- What is GPIO?
- Difference between Input and Output?
- What is Logic HIGH?
- What is Logic LOW?
- What is a Floating Input?
- Why do we use Pull-up resistors?
- What is Active LOW?
- Difference between Push-Pull and Open-Drain?

### Intermediate

- Explain GPIO Registers.
- Why are floating inputs dangerous?
- Why does I²C use Open-Drain?
- What is the purpose of the PUPDR register?

---

# 📚 References

- ARM Cortex-M Documentation
- STM32 Reference Manual
- STM32 Datasheet
- Arduino Documentation
- ESP32 Technical Reference Manual

---

# 🎯 Key Takeaways

- GPIO is the bridge between a microcontroller and the external world.
- Input pins read signals; Output pins drive signals.
- Logic HIGH and LOW represent digital states.
- Floating inputs cause unpredictable behavior.
- Pull-up and Pull-down resistors provide stable logic levels.
- Push-Pull and Open-Drain outputs serve different applications.
- GPIO registers configure and control pin behavior.
- Understanding GPIO is essential before learning communication protocols and peripherals.

---

# ⏭️ Next Topic

## 🚀 Day 03 — Binary Numbers, Bitwise Operations & Registers

Topics:

- Binary Number System
- Decimal ↔ Binary Conversion
- Hexadecimal
- Bitwise Operators
- Bit Masking
- Setting, Clearing & Toggling Bits
- Shift Operators
- Register Manipulation

---

<div align="center">

## ⭐ Day 02 Complete

*"Every LED that blinks, every button that responds, and every sensor that communicates begins with GPIO."* ⚡

</div>