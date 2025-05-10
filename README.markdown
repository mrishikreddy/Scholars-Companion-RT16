# A Student Thing

Welcome to **A Student Thing**, a C-based console application designed to assist students with academic tasks and provide a bit of fun along the way. This project, created by Rishik and Anji, offers tools to estimate internal marks, manage attendance, and play a classic Tic-Tac-Toe game against the computer. It's a simple yet practical utility for students looking to stay on top of their academic game.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
  - [Internal Marks Estimator](#internal-marks-estimator)
  - [Attendance Manager](#attendance-manager)
  - [Tic-Tac-Toe Game](#tic-tac-toe-game)

## Features
- **Internal Marks Estimator**: Calculate the marks needed in your second mid-term to achieve a target internal score.
- **Attendance Manager**: Track attendance across subjects and determine how many classes you need to attend to reach 75% attendance.
- **Tic-Tac-Toe Game**: Play a fun game of Tic-Tac-Toe against a computer opponent with a basic AI.
- User-friendly console interface with clear menus and prompts.
- Cross-platform compatibility (with minor adjustments for non-Windows systems).

## Installation
To get started with **A Student Thing**, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/a-student-thing.git
   cd a-student-thing
   ```

2. **Compile the Code**:
   Ensure you have a C compiler installed (e.g., GCC). Compile the source code using:
   ```bash
   gcc -o student_thing main.c -lm
   ```
   Note: The `-lm` flag links the math library, required for functions like `round()`.

3. **Run the Program**:
   On Windows:
   ```bash
   student_thing.exe
   ```
   On Linux/Mac:
   ```bash
   ./student_thing
   ```

   **Note**: The program uses `conio.h` and `unistd.h`, which are not standard across all platforms. For non-Windows systems, you may need to replace `getch()` with a standard input function and remove or emulate `system("cls")` for screen clearing.

## Usage
Once the program runs, you'll see the main menu:
```
                A STUDENT THING
                        -An innovation from Rishik

                Press:
                  1  to estimate internal marks
                  2  to know how to maintain attendance
                  3  to play a game
                  4  to exit

                Your choice:
```
- Enter a number (1–4) to select an option.
- Follow the on-screen prompts to input data or make choices.
- After each task, choose to repeat, return to the main menu, or exit.

## How It Works

### Internal Marks Estimator
- **Purpose**: Helps students estimate the marks needed in their second mid-term to achieve a desired total internal score.
- **Input**:
  - Your target internal marks for the semester.
  - First mid-term marks for subjects like PSP, AP/EMMS, EM, EP LAB, ELE, APTT/ES, and PSP LAB.
- **Output**: Displays the required second mid-term marks for each subject to meet the target, or indicates if the target is unreachable.
- **Logic**: Uses a formula to calculate the contribution of first and second mid-term marks (75% and 25% weightage, respectively) to the total internal score.

### Attendance Manager
- **Purpose**: Calculates how many additional classes you need to attend to achieve 75% attendance in each subject.
- **Input**:
  - Current day and month.
  - Current attendance percentage for subjects (APTT, AP, EM, EP LAB, ELE, PSP, PSP LAB, PPC).
- **Output**: A table showing:
  - Current attendance percentage.
  - Total periods held and attended.
  - Number of periods needed to reach 75% attendance (or a note if already above 75%).
- **Logic**: Tracks periods based on a predefined schedule (hardcoded for April and May) and calculates required attendance using the formula: `((75 * total_periods) - (100 * attended_periods)) / 25`.

### Tic-Tac-Toe Game
- **Purpose**: Offers a fun break by letting you play Tic-Tac-Toe against a computer.
- **Input**:
  - Player name.
  - Number (1–9) to place your 'X' on the board.
- **Output**: Displays the game board, announces the winner (or draw), and offers options to replay, return to the main menu, or exit.
- **Computer AI**: Uses a simple rule-based strategy to block player wins or prioritize winning moves, falling back to predefined position preferences (e.g., center, corners, edges).
- **Logic**: Checks for wins or draws after each move using predefined winning combinations.

Feel free to explore **A Student Thing** and make it your own. If you have questions or suggestions, open an issue or reach out. Happy studying (and gaming)!
