# MiniSQL: Compiler Design Parser & Query Processing

A web-based Interactive SQL Compiler and Query Processor designed to visualize the step-by-step compilation pipeline (Lexical Analysis, Syntax Analysis, and Execution) of SQL queries. Built as a laboratory mini-project for Compiler Design, it features an elegant, real-time UI built with Tailwind CSS and a lightweight but powerful analytical backend driven by Python & Flask.

## ✨ Key Features

1. **Integrated Development Environment (IDE)**
   - A dark-mode SQL code editor block simulating a terminal IDE.
   - Built-in expandable query **History** and **Examples** panels.
2. **Detailed Compilation Pipeline**
    - A live pipeline indicator tracking the status of tokens, syntax parsing, and final execution (`Green = Success`, `Red = Failure`).
3. **Lexical Analysis (Tokenizer)**
   - Custom Python Regular Expression logic that parses complex raw SQL strings.
   - Accurately identifies Tokens & Lexemes into types: `KEYWORD`, `IDENTIFIER`, `STRING`, `NUMBER`, `OPERATOR`, `SYMBOL`, and `WILDCARD`.
4. **Syntax Analysis (Abstract Syntax Tree)**
   - Evaluates token streams against a custom grammar.
   - Fully visual Custom AST SVG graph rendered directly in the browser via JavaScript recursion. Top-down, node-based flowchart mapping elements.
5. **Execution Engine**
   - Contains an in-memory dictionary-based mock database supporting:
     - `CREATE TABLE`
     - `INSERT INTO`
     - `SELECT` (Including specific columns, wildcards `*`, and `WHERE .. AND` clauses)
     - `UPDATE`
     - `DELETE`
     - `DROP TABLE`

## 🚀 Tech Stack

- **Frontend:** HTML5, Vanilla JavaScript, Tailwind CSS (via CDN), Google Material Symbols.
- **Backend Architecture:** Python, Flask server, Regex standard libraries.
- **Data Persistence:** In-memory application memory state for query execution results.

## 📦 Setup & Installation

### Requirements
- Python 3.8+


### Running Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/dilpreet579/cd-mini-project.git
   cd cd-mini-project
   ```

2. **Create and activate a virtual environment (Recommended):**
   ```bash
   # Windows (PowerShell)
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   
   # Linux/MacOS
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install the dependencies:**
   ```bash
   pip install Flask
   ```

4. **Start the Flask server:**
   ```bash
   python app.py
   ```

5. **Open the interface:**
   Go to your preferred web browser and navigate to: `http://127.0.0.1:5000/`

## 🖥️ Usage

1. Open the application.
2. In the query terminal window (`query.sql`), enter a valid SQL query or select a pre-made query from the **Examples** sidebar (accessible by clicking the lightbulb icon).
3. Click **Run**.
4. Observe the `Pipeline` indicator dynamically update based on if a token syntax error or database violation (e.g. Table does not exist) is passed.
5. Swap between the output tabs (`Tokens` / `AST`):
    - The **Tokens Tab** displays a table mapping token streams dynamically.
    - The **AST Tab** features both an interactive graphical Syntax tree plot and a raw JSON structural payload.

## 🤝 Project Information
This application was developed as a comprehensive educational tool for a **Compiler Design Laboratory Assignment** to demonstrate how languages parse token streams, enforce grammatical rules, generate abstract structure trees, and ultimately execute programmatic intent.

---
**Developed by:** 
- Ishita Gupta (231210050)
- Dilpreet Singh (231210041)