# Assignment 1 – Transliteration Accuracy Testing
### IT3040 – IT Project Management | BSc (Hons) in Information Technology | Year 3, Semester 1

---

## 📖 Project Overview

This project implements an automated testing solution using **Python and Playwright** to evaluate the accuracy of the **Chat Sinhala transliteration** feature of the following application:

🔗 https://www.pixelssuite.com/chat-translator

The objective is to identify scenarios where the system **fails** to correctly convert chat-style Singlish input into Sinhala output.

A total of **50 negative test cases** were designed, ensuring coverage of all **24 Singlish input types** specified in the assignment guidelines.

Note: This project only evaluates the **Chat Sinhala** transliteration function. Standard Sinhala transliteration, backend APIs, and performance/scalability/security testing are outside the scope of this assignment.

---

## ⚙️ Prerequisites

Ensure the following are installed on your machine before running the tests:

- **Python** 3.11 or 3.12 — https://www.python.org/downloads/
- **pip** (comes included with Python)
- **Google Chrome** browser 

---

## 📦 Setup Instructions

### 1. Clone or Download the Repository
Download the project ZIP from this repository and extract it to your local machine.

### 2. Open Command Prompt or VS Code Terminal
- **Command Prompt:** Press `Windows Key + R`, type `cmd`, press Enter
- **VS Code:** Open the project folder in VS Code and open the terminal

### 3. Navigate to the Project Folder
Replace `YOUR_PATH` with the actual location where you extracted the folder:
```
cd /d YOUR_PATH\test_automation
```
Example:
```
cd /d D:\test_automation
```

### 4. Install Dependencies
Run the following commands one by one:
```
pip install -U pip
```
```
pip install playwright openpyxl
```
```
playwright install
```

---

## 📝 Excel File Preparation

Open the file inside the project folder:
```
Assignment 1 - Test cases.xlsx
```

Ensure the following columns are filled before running the script:

| Column | Header | Description |
|--------|--------|-------------|
| A | TC ID | Test case identifier (e.g. Neg_0001) |
| B | Input length type | S (≤ 30 chars), M (31–299 chars), L (300–450 chars) |
| C | Input | The Singlish input text to be tested |
| D | Expected output | The correct expected Sinhala translation |

> ⚠️ Do **NOT** manually fill in **Actual output** or **Status** columns — these are filled in automatically by the script.

---

## ▶️ Running the Test Script

Make sure you are inside the `test_automation` folder in your terminal, then run:

```
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

---

## 🔍 What the Script Does

1. Opens the web application in Google Chrome
2. Enters each Singlish input from the Excel file automatically
3. Captures the actual Sinhala output from the application
4. Compares it with the expected output
5. Automatically records the following back into the Excel file:
   - **Actual output** — what the application actually produced
   - **Status** — PASS or FAIL

---

## 📊 Viewing Results

After the script finishes running:

1. Open `Assignment 1 - Test cases.xlsx`
2. Check the following columns:
   - **Column E — Actual output** — filled automatically by the script
   - **Column F — Status** — PASS or FAIL filled automatically by the script

---

## 📁 Project Structure

```
test_automation/
│
├── test_automation.py               # Main Playwright automation script
├── Assignment 1 - Test cases.xlsx   # Excel file with all 50 test cases


```

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| Python 3.11 / 3.12 | Programming language used for automation |
| Playwright (Python) | Browser automation framework |
| openpyxl | Library for reading and writing Excel files |
| Google Chrome | Browser used during test execution |
| Microsoft Excel | Test case documentation and results recording |

---

## 🎓 Assignment Details

| Detail | Information |
|--------|-------------|
| Degree | BSc (Hons) in Information Technology |
| Year / Semester | Year 3, Semester 1 |
| Course | IT3040 – IT Project Management |
| Assignment | Assignment 1 – Option 1 |

---

## 👤 Author

**Kaunarathna P W J P**

BSc (Hons) in Information Technology – Year 3
SLIIT
