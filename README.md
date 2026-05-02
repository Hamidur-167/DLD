# DLD
# 🔐 4-Digit Smart Door Lock System

A **microcontroller-free digital door lock system** built using pure digital logic circuits and 74-series ICs.  
This project demonstrates how a secure 4-digit password-based access system can be designed using logic gates, flip-flops, counters, comparators, timers, and seven-segment displays.

---

## 📌 Project Overview

The **4-Digit Smart Door Lock System** is an electronic access control system that allows a user to unlock a door by entering a predefined 4-digit PIN.

Unlike many modern smart locks, this system does **not use any microcontroller**. Instead, it relies entirely on digital logic ICs, making it a cost-effective, educational, and hardware-focused solution.

---

## ✨ Features

- 🔢 **4-digit password authentication**
- 🚫 **No microcontroller required**
- 🧠 Built using **combinational and sequential logic**
- 📟 **7-segment display** for input feedback
- ✅ Green LED indication for correct password
- ❌ Red LED indication for incorrect attempts
- 🔒 Lockout system after multiple wrong attempts
- ⏱️ 555 timer-based temporary freeze mechanism
- 🔁 Reset option for fresh input
- 💰 Low-cost and power-efficient design

---

## 🛠️ Technologies & Components Used

### Main ICs

| Component | Purpose |
|---|---|
| 7485 | 4-bit magnitude comparator for password matching |
| 7447 | BCD to 7-segment display decoder |
| 74194 | Shift register |
| 4013 | D flip-flop |
| 4043 | Latch |
| 4017 | Decade counter |
| 4066 | Analog switch |
| 4555 | Decoder/demultiplexer |
| 555 Timer | Lockout timing mechanism |
| 4011 / 4072 / 7408 | Logic gate operations |

### Other Components

- Push buttons
- Breadboards
- Jumper wires
- LEDs
- Resistors
- Capacitors
- 7-segment displays
- 5V DC power supply

---

## ⚙️ Working Principle

The system works in four major stages:

### 1. Password Input

The user enters a 4-digit PIN using push buttons arranged as keypad inputs.  
The entered digits are processed and stored temporarily using digital ICs.

### 2. Password Comparison

The entered password is compared with the preset password using **7485 magnitude comparator ICs**.

- If the entered code matches the stored code, the unlock signal is generated.
- If the entered code is wrong, the system registers an incorrect attempt.

### 3. Feedback System

The system provides visual feedback:

- ✅ **Green LED** turns on for a correct password.
- ❌ **Red LED** turns on after incorrect attempts.
- 📟 **7-segment displays** show the entered digits.

### 4. Security Lockout

After three consecutive incorrect attempts, the system activates a temporary lockout using a **555 timer**.  
During this period, the system freezes for approximately **10–11 seconds** and ignores further inputs.

---

## 🧪 Experimental Results

The system was tested under different input conditions.

| Test Case | Result |
|---|---|
| Correct password entered | Green LED turned on and unlock signal activated |
| Incorrect password entered | Input rejected |
| Three wrong attempts | Red LED activated and system locked temporarily |
| Reset after lockout | System returned to normal state |
| Power usage | Low-power operation observed |

The system performed reliably during hardware testing and successfully validated correct passwords while rejecting incorrect ones.

---

## 📷 Hardware Implementation

The circuit was implemented on breadboards using multiple digital ICs, logic gates, seven-segment displays, push buttons, and LEDs.

> Add your hardware image here:

```html
<img src="images/hardware.jpg" alt="Hardware Implementation" width="600">
