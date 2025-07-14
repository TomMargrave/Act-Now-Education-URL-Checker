# Act-Now-Education-URL-Checker
A Python tool to extract links from an HTML table, check if they are valid or broken, and save the results to CSV and Excel files. No coding experience required—just copy, run, and review the report.
chg nothing


# ActNowEd URL Table Extractor & Validator
## Table of Contents

- [Act-Now-Education-URL-Checker](#act-now-education-url-checker)
- [ActNowEd URL Table Extractor \& Validator](#actnowed-url-table-extractor--validator)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [How to Get the Input HTML File](#how-to-get-the-input-html-file)
  - [Installation (Windows, Linux, macOS)](#installation-windows-linux-macos)
    - [1. Install Python](#1-install-python)
    - [2. Open a Terminal](#2-open-a-terminal)
    - [3. Install Required Packages](#3-install-required-packages)
  - [How to Run the Script](#how-to-run-the-script)
  - [Output and Results](#output-and-results)
  - [Output and Results](#output-and-results-1)
  - [Troubleshooting](#troubleshooting)

---

## Overview

This script helps Act Now Education group validate links on Career Compass by:
- Extract links from a table in an HTML file.
- Check if those links are working.
- Save the results in Excel and CSV files.

You do **not** need any coding experience to use this guide.

---

## How to Get the Input HTML File

1. **Open the website** with the table you want to extract in Google Chrome.
2. **Right-click** on the table and choose **Inspect** (or press `F12` to open Developer Tools).
3. In the Elements panel, **right-click the `<table>` element** (make sure you have the whole table selected).
4. Choose **Copy > Copy outerHTML**.
5. **Open Notepad** (Windows), **TextEdit** (macOS in plain text mode), or any text editor.
6. **Paste** the copied HTML.
7. **Save the file** as `element.html` in the same folder as the script.

---

## Installation (Windows, Linux, macOS)

### 1. Install Python

- Download Python from [python.org](https://www.python.org/downloads/).
- Install it. On Windows, make sure to check **"Add Python to PATH"** during installation.

### 2. Open a Terminal

- **Windows:** Press `Win + R`, type `cmd`, and press Enter.
- **macOS:** Open **Terminal** from Applications > Utilities.
- **Linux:** Open your terminal emulator.

### 3. Install Required Packages

Copy and paste this command into your terminal and press Enter:
````
pip install beautifulsoup4 requests openpyxl
````
If you have both Python 2 and 3, you may need to use `pip3` instead:
````
pip3 install beautifulsoup4 requests openpyxl
````

---

## How to Run the Script

1. **Place your `element.html` file** in the same folder as the script (`ParseHTML_and_Validate.py`).
2. In your terminal, **navigate to the folder** where the script is saved. For example:
   - Windows:
     ```
     cd path\to\your\folder
     ```
   - macOS/Linux:
     ```
     cd /path/to/your/folder
     ```
3. **Run the script** by typing:
   ```
   python ParseHTML_and_Validate.py
   ```
  or, if you use `python3`:
   ```
   python3 ParseHTML_and_Validate.py
   ```
   
4. **Results:**  
- `urls.csv` and `url_validation_report.xlsx` will be created in the same folder.

---

## Output and Results

After running the script, you will find two new files in the same folder as the script:

- **urls.csv** — Contains all the links extracted from your HTML table.
- **url_validation_report.xlsx** — An Excel file with three sheets:
  - **All URL Results**: Every link and its status.
  - **Broken URLs**: Only links that are broken or have errors.
  - **Valid URLs**: Only links that are working.

At the end of the script, you will also see a summary printed in the terminal, for example:

4. **Results:**  
- `urls.csv` and `url_validation_report.xlsx` will be created in the same folder.

---

## Output and Results

After running the script, you will find two new files in the same folder as the script:

- **urls.csv** — Contains all the links extracted from your HTML table.
- **url_validation_report.xlsx** — An Excel file with three sheets:
  - **All URL Results**: Every link and its status.
  - **Broken URLs**: Only links that are broken or have errors.
  - **Valid URLs**: Only links that are working.

At the end of the script, you will also see a summary printed in the terminal, for example:
📊 URL Validation Summary: 
Total URLs : 452 
Valid URLs : 180 39.82% 
Redirected : 123 27.21% 
Broken URLs : 129 28.54% 
Redirected HTTP: 20 4.42%

**What this means:**
- **Total URLs**: The number of links checked.
- **Valid URLs**: Links that work and return a successful response.
- **Redirected**: Links that automatically send you to a different address.
- **Broken URLs**: Links that do not work or return an error.
- **Redirected HTTP**: Links that were redirected from HTTP to HTTPS.

You can open the Excel file to see detailed results for each link.

---

## Troubleshooting

- **"python not found" or "pip not found":**  
  Python may not be installed or not added to your PATH. Reinstall Python and check "Add to PATH" during setup.

- **ImportError (e.g., No module named 'openpyxl'):**  
  Run the install command again:
  ```
  pip install openpyxl
  ```

- **Import "openpyxl" could not be resolved from source (Pylance):**  
In VS Code, select the correct Python interpreter:
  - Press `Ctrl+Shift+P`, type `Python: Select Interpreter`, and choose the one where you installed the packages.

- **Permission denied or file not found:**  
Make sure you are in the correct folder and have permission to read/write files.

- **No table found in the HTML file:**  
Double-check that your `element.html` file contains a `<table>` element. Try copying the table HTML again.

- **Still stuck?**  
- Make sure your input file is named `element.html` and is in the same folder as the script.
- Try running the script as administrator (Windows: right-click Command Prompt > Run as administrator).

---


