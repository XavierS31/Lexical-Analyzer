# PL/0 Lexical Analyzer — COP 3402 System Software

Lexical Analyzer implemented in **C** for the **PL/0 programming language**, developed as part of **COP 3402 – System Software (Fall 2025)** at the University of Central Florida under **Dr. Jie Lin**.

This program reads a PL/0 source file, tokenizes its contents, and outputs three sections:
1. **Source Program** (verbatim copy)
2. **Lexeme Table** (token–type mapping)
3. **Token List** (numeric representation)

---

## 📘 Project Overview

This project implements the **first phase of a compiler**, known as **lexical analysis (scanning)**.

It performs:
- Character-by-character reading of a PL/0 program.
- Token recognition (identifiers, reserved words, numbers, symbols).
- Detection and reporting of lexical errors:
  - Identifiers longer than **11 characters**.
  - Numbers longer than **5 digits**.
  - Invalid symbols not part of the PL/0 alphabet.
- Skipping of comments (`/* ... */`) and whitespace.

The output format **exactly matches** the COP 3402 assignment specification.

---

## ⚙️ Features

✅ Identifies and categorizes:
- **Reserved words** (`begin`, `end`, `if`, `then`, `var`, …)
- **Identifiers** (up to 11 characters)
- **Numbers** (up to 5 digits)
- **Special symbols** (`+`, `-`, `:=`, `<`, `<=`, `<>`, `>`, `>=`, etc.)

⚠️ Reports lexical errors:
- `Identifier too long`
- `Number too long`
- `Invalid Symbol`

🧩 Handles comments and whitespace:
- Skips multi-line comments: `/* comment */`
- Skips spaces, tabs, and newlines.

---

## 🖥️ Usage

### 🧱 Compilation
```bash
gcc -O2 -std=c11 -o lex lex.c
