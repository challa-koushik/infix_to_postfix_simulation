
# Infix to Postfix Expression Simulator (Qt C++ GUI)
## Hybrid Professional + Student-Friendly README (Advanced)

Welcome to the **Infix to Postfix Expression Simulator**, an interactive Qt-based C++ application that visually demonstrates how infix expressions are converted into postfix (Reverse Polish Notation) using a stack.

This README blends **professional open‑source formatting** with **student-friendly explanations**, making it perfect for GitHub, academic submission, and viva preparation.

---

# Project Summary

This project provides a **step-by-step visual simulation** of the classic *Infix → Postfix* conversion algorithm using:

- **Qt Widgets (C++ GUI)**
- **Stack-based evaluation**
- **Clean layouts & minimalistic UI**
- **ASCII-based stack visualization**
- **Vertical token breakdown**

It helps students understand:
- Operator precedence  
- Associativity rules  
- Stack operations  
- Expression parsing  

---

# Key Features

### **1. Step-by-Step Simulation**
Each symbol of the infix expression is processed one step at a time.

Shows:
- Current character  
- Stack contents  
- Output so far  
- Explanation of action  

---

### **2. Visual Stack Representation**
Operators pushed onto the stack are shown using ASCII boxes:

```
┌───────┐
│   *   │
└───────┘
┌───────┐
│   +   │
└───────┘
```

Top element is highlighted for clarity.

---

### **3. Vertical Token Breakdown**
Expression like `A+B*C` becomes:

```
A
+
B
*
C
```

The current token is automatically highlighted.

---

### **4. Clean UI (Beginner-Friendly Layout)**
- No complex styling  
- Simple layouts  
- Highly readable simulation steps  

---

### **5. Robust Error Handling**
- Empty input check  
- Unicode operator normalization  
- Invalid character prevention  

---

# Algorithm Overview (High-Level)

The system follows the standard **Shunting Yard Algorithm**:

### ➤ Rule 1: Operands → output  
### ➤ Rule 2: Operators → push to stack  
(based on precedence and associativity)

### ➤ Rule 3: '(' → push  
### ➤ Rule 4: ')' → pop until '('  
### ➤ Rule 5: At the end → pop remaining operators  

A full explanation appears in the "Explanation Box" during the simulation.

---

# GUI Layout Diagram (Conceptual)

```
 ---------------------------------------------------------
|  Infix Input: [ A+B*C ]     [ Start ] [ Next ] [ Clear ] |
 ---------------------------------------------------------
|  INPUT CHARS     |             STACK TABLE               |
|  A               |         ┌───────┐                     |
|  +               |         │   *   │                     |
|  B               |         └───────┘                     |
|  *               |         ┌───────┐                     |
|  C               |         │   +   │                     |
|                  |         └───────┘                     |
 ---------------------------------------------------------
| Output: ABC*+                                         |
 ---------------------------------------------------------
| Explanation:                                          |
| '*' has higher precedence; push to stack              |
 ---------------------------------------------------------
```

---

# Project Structure

```
 Infix-Postfix-Simulator/
 ├── CMakeLists.txt
 ├── main.cpp
 ├── simwindow.h
 ├── simwindow.cpp
 ├── README.md  (this file)
 └── screenshots/
```

---

# Build & Run Instructions

## **Using Terminal (Linux / WSL / macOS)**

### Step 1 — Create build folder
```bash
mkdir build
cd build
```

### Step 2 — Configure project
```bash
cmake ..
```

### Step 3 — Compile
```bash
make -j$(nproc)
```

### Step 4 — Run
```bash
./infix-postfix-sim
```

---

## Using Qt Creator (Recommended for Students)

1. Open **Qt Creator**  
2. Click **Open Project** → select `CMakeLists.txt`  
3. Wait for configuration  
4. Press **Run**  

---

# Technologies Used

| Component | Purpose |
|----------|----------|
| **Qt Widgets** | GUI framework |
| **QMainWindow** | Main application window |
| **QLineEdit** | Input/output text fields |
| **QTableWidget** | Stack visualization |
| **QListWidget** | Vertical input token display |
| **QTextEdit** | Explanation area |
| **QStack** | Core stack logic |
| **QVector** | Step storage |

---

# Viva Preparation Notes

### Why Qt?
- GUI is easier for students to understand than console  
- Qt provides built-in widgets  
- Cross-platform  
- Signal-slot mechanism simplifies event handling  

### What is the purpose of the project?
“To visually demonstrate the infix-to-postfix conversion using stack operations in a clear, interactive way.”

### Why show input vertically?
- Helps understand token-by-token processing  
- Matches manual evaluation method taught in class  

### Why ASCII stack boxes?
- Makes stack operations intuitive  
- Shows push/pop clearly  

---

# Team Members

| Name | Roll No |
|------|---------|
| **Challa Koushik** | AP24110012141 |
| **R. Sruthi Laya** | AP24110012135 |
| **Shaik Aslimaan Thaslimaan** | AP24110012131 |
| **P. Anu Sathvika** | AP24110012125 |

---

# Contribution Roles

### **Koushik**
- Qt window setup  
- Stack visualization logic  

### **Sruthi Laya**
- Algorithm breakdown and testing  
- Input validation  

### **Aslimaan**
- UI layout improvements  
- Explanation messages  

### **Anu Sathvika**
- Documentation & report work  
- README preparation  

---

# License
Academic use only. Free for learning and teaching.

---

# Final Note

If you're a student learning Data Structures, this simulation will help you **understand exactly how infix expressions are converted internally** — with stack operations visible at each step.

Enjoy learning!

``Installing Environment``
step 1:

open terminal in windows
"wsl --install " run this comand

//after installation
step-2:

sudo apt update
sudo apt upgrade -y

step 3:

"sudo apt install -y build-essential"

step 4:

"sudo apt install -y cmake "

step-5:

"cmake --version "
You should see something like:
"cmake version 3.xx.x"

step-6:

"sudo apt install -y qtbase5-dev qt5-qmake qttools5-dev-tools"

step 7:

open vs code of the project folder and (ctrl + shift + p)
thenyou will see "wsl reload/reopen"

step-8:

mkdir build
cd build
cmake ..
make
./infix-postfix-sim
