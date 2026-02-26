# 🔐 ContextLock – Multi-Layer Secure Digital Lock System

ContextLock is a **hardware-oriented digital security system** designed using **combinational and sequential logic principles**.  
Unlike traditional password-only digital locks, this system integrates **time-based access control, attempt speed monitoring, and attempt limitation** to provide enhanced multi-layer hardware security.

The system was designed and verified using **Logisim-Evolution simulation**.

---

## 📌 Project Overview

* **Domain**: Digital Electronics / Hardware Security
* **Focus**: Context-Aware Access Control
* **Design Approach**: Combinational + Sequential Logic
* **Simulation Tool**: Logisim-Evolution
* **Security Layers**:
  - Password Verification
  - Time-Based Access Control
  - Attempt Speed Monitoring
  - Attempt Limitation & Lockout

---

## 🚀 Key Features

* 🔑 4-bit Password Authentication
* ⏰ 24-hour Time-Based Access Restriction
* ⚡ Attempt Speed Monitoring (anti-rapid entry protection)
* 🔁 Maximum Attempt Limitation (≤ 3 attempts)
* ⛔ Automatic Lockout Mechanism
* 🔓 Unlock only when ALL conditions are satisfied
* 💡 LED-based Output Verification
* 🧪 Fully verified using simulation scenarios

---

## 🛠️ Components Used

* 4-bit Comparators
* Magnitude Comparators
* 4-bit Counter (Attempt Counter)
* 5-bit Counter (Time Counter)
* Interval Counter (Speed Monitoring)
* Registers
* AND Gates
* NOT Gates
* LEDs
* Logic Probes

---

## 🧠 System Logic

The unlock signal is generated only when **all security conditions evaluate to TRUE simultaneously**.

```
UNLOCK = PasswdOK ∧ time_ok ∧ speed_ok ∧ attempts_ok
```

If any condition fails, access is denied.

---

## 🏗️ System Architecture

```
START
   ↓
Password Verification ──► PasswdOK
Time-Based Access ───────► time_ok
Speed Monitoring ────────► speed_ok
Attempt Counter ─────────► attempts_ok
                 ↓
            AND Gate
                 ↓
              UNLOCK
```

Each validation block operates independently and feeds its output into the final AND gate decision logic.

---

## 🧪 Simulation & Testing

The system was tested under multiple conditions:

* ✅ Correct password & valid time → Unlock
* ❌ Incorrect password → Access denied
* ⏰ Outside allowed time → Access denied
* ⚡ Rapid attempts → Rejected
* 🔁 More than 3 attempts → Lockout activated

LED indicators and logic probes were used to confirm signal behavior during simulation.

---

## 🎯 Concepts Applied

* Combinational Logic Design
* Sequential Logic Design
* Counters & Registers
* Magnitude Comparators
* Multi-Factor Hardware Authentication
* Parallel Condition Evaluation
* AND-Gate Based Decision Logic

---

## 📜 Licence

This project was developed as part of a **ADLD Laboratory / SEE EL** to demonstrate practical implementation of multi-layer hardware security mechanisms.
