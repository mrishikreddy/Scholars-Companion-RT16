# A STUDENT THING

**A STUDENT THING** is a simple, console-based C project designed to assist students with essential academic utilities. It bundles three tools into one program:

1. 📊 **Internal Marks Estimation**  
2. 📅 **Attendance Tracking**  
3. ❌⭕ **Tic Tac Toe Game** (single-player against a basic AI)

This project was developed by Rishik and Anji as a learning exercise in C.

---

## 📑 Table of Contents

- [Features](#features)  
- [Requirements](#requirements)  
- [Build & Run](#build--run)  
- [Usage](#usage)  
- [Contributing](#contributing)  
- [License](#license)  
- [Acknowledgments](#acknowledgments)  
- [Contact](#contact)  

---

## ✨ Features

### 1. Internal Marks Estimator  
- Prompts for your **target internal total** (out of 60)  
- Takes **Mid-1** scores for PSP, AP/EMMS, EM, EP Lab, ELE, APTT/ES, PSP Lab (each out of 40)  
- Calculates the **estimated Mid-2** marks needed to reach the target, choosing between two strategies  
- Warns if the target is unreachable (even with a perfect Mid-2 score)

### 2. Attendance Tracker  
- Prompts for a **date** (day & month—supports April and May)  
- Simulates total periods held per subject up to that date  
- Takes current **attendance percentage** for 8 subjects: APTT, AP, EM, EP Lab, ELE, PSP, PSP Lab, PPC  
- Calculates and displays:
  - Periods held  
  - Periods attended  
  - Additional periods needed to reach **75%** (or notes if already ≥ 75%)

### 3. Tic Tac Toe Game  
- Classic 3×3 grid in console  
- Player (X) vs computer AI (O)  
- Basic AI that tries to win or block based on pattern checks  
- Detects **win**, **draw**, and offers **replay** or return to main menu  

---

## 🛠️ Requirements

- **C compiler**: `gcc`, `clang`, or equivalent  
- **Terminal** or **Command Prompt**  
- Optionally on Windows, ensure you have access to `<conio.h>` (or replace `getch()` calls)

---

## 🚀 Build & Run

1. **Compile**  
   ```bash
   gcc student_thing.c -o student_thing
