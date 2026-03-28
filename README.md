Here's the complete `README.md` content for your **Password Strength Analyzer — Cyber Recon Edition v2.0**:

---

```markdown
# 🔐 Password Strength Analyzer — Cyber Recon Edition v2.0

```
██████╗  █████╗ ███████╗███████╗
██╔══██╗██╔══██╗██╔════╝██╔════╝
██████╔╝███████║███████╗███████╗
██╔═══╝ ██╔══██║╚════██║╚════██║
██║     ██║  ██║███████║███████║
╚═╝     ╚═╝  ╚═╝╚══════╝╚══════╝

██╗  ██╗ █████╗  ██████╗██╗  ██╗
██║  ██║██╔══██╗██╔════╝██║ ██╔╝
███████║███████║██║     █████╔╝
██╔══██║██╔══██║██║     ██╔═██╗
██║  ██║██║  ██║╚██████╗██║  ██╗
╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝
```

> **A terminal-based password strength analysis and generation tool with a full hacker-aesthetic UI — built for Kali Linux / VMware environments.**

---

## 📌 Overview

**PASS HACK** is a feature-rich, cybersecurity-themed password analysis tool written in Python. It provides real-time entropy calculation, brute-force resistance estimation, pattern detection, SHA-256 fingerprinting, batch scanning, and strong password generation — all wrapped in a matrix-rain, ANSI-colored terminal UI.

---

## 🖥️ Requirements

| Requirement | Version |
|-------------|---------|
| Python      | 3.6+    |
| OS          | Linux / Kali Linux / VMware |
| Terminal    | ANSI-color-capable (e.g., bash, zsh, xterm) |

### Standard Library Only — No pip installs needed!

All modules used are part of Python's standard library:

```
re, sys, time, math, random, string, hashlib, os
```

---

## 🚀 Installation & Usage

### 1. Clone or Download

```bash
git clone https://github.com/yourname/pass-hack.git
cd pass-hack
```

### 2. Make Executable

```bash
chmod +x passhack.py
```

### 3. Run

```bash
python3 passhack.py
```

Or directly:

```bash
./passhack.py
```

---

## 🎯 Features

### ✅ Password Analyzer
- Real-time **entropy calculation** (bits)
- **Brute-force time estimation** at 10 billion guesses/second (GPU-level)
- **Character composition** check (lowercase, uppercase, digits, symbols)
- **Pattern detection** — keyboard walks, sequences, repeated chars, year patterns
- **Breach database** check against 50+ known common passwords
- **SHA-256 fingerprint** generation
- **Strength score** (0–100) with color-coded status bar

### 🗂️ Batch Scanner (from file)
- Load a `.txt` file with one password per line
- Get a quick summary report for every password
- Displays entropy, score, label, and masked password

### 🔑 Password Generator
- Specify custom length (minimum: 12)
- Guarantees at least one of: lowercase, uppercase, digit, symbol
- Shuffled randomly using `secrets`-equivalent logic
- Instant full analysis report on the generated password

### 🌐 Cyber UI Effects
- **Matrix rain** animation on startup
- **Glitch text** intro effect
- **Animated scan bars** for each analysis stage
- **Pulsing status** indicators
- Full ANSI color-coded terminal output

---

## 📊 Strength Score Breakdown

| Score Range | Status Label        | Description              |
|-------------|---------------------|--------------------------|
| 80–100      | 🟩 FORTRESS          | Very Strong — excellent  |
| 60–79       | 🟨 GUARDED           | Strong — good coverage   |
| 40–59       | 🟨 EXPOSED           | Moderate — improvable    |
| 20–39       | 🟥 CRACKABLE         | Weak — risky             |
| 0–19        | 🔴 BREACHED          | Critical — change ASAP   |

---

## 🔢 Entropy Calculation

Entropy is computed as:

```
Entropy (bits) = Length × log₂(CharsetPool)
```

| Character Set  | Pool Size |
|----------------|-----------|
| Lowercase a–z  | +26       |
| Uppercase A–Z  | +26       |
| Digits 0–9     | +10       |
| Symbols        | +32       |

---

## ⏱️ Brute-Force Time Estimation

Assumes **10 billion guesses/second** (modern GPU):

```
Time = (2 ^ entropy_bits) / 10,000,000,000
```

| Time Range       | Rating     |
|------------------|------------|
| < 1 second       | 🔴 INSTANT |
| Seconds–Minutes  | 🔴 Critical|
| Hours–Days       | 🟡 Weak    |
| Years            | 🟢 Strong  |
| Centuries+       | 🟢 Fortress|

---

## 🚨 Pattern Detection

The tool flags the following dangerous patterns:

| Pattern Type          | Example          |
|-----------------------|------------------|
| Repeated characters   | `aaa`, `111`     |
| Sequential strings    | `abc`, `123`     |
| Keyboard walks        | `qwerty`, `asdf` |
| Common words          | `password`, `admin` |
| Year patterns         | `1998`, `2024`   |

---

## 📁 Batch Scan File Format

Create a plain `.txt` file with one password per line:

```
mypassword123
P@ssw0rd!
hunter2
Tr0ub4dor&3
```

Then choose **Option 2** from the menu and provide the file path.

---

## 🛡️ Security Notes

- ✅ Passwords are **never stored or logged**
- ✅ Hashing is one-way SHA-256 — only used as a visual fingerprint
- ✅ No network connections are made — fully **offline**
- ✅ Generated passwords are **not saved anywhere**
- ⚠️ Do **not** use real production passwords in demo/shared environments

---

## 📸 UI Preview

```
╔════════════════════════════════════════════════════════════╗
║  ▓▓  PASS HACK — CYBER RECON EDITION  v2.0  ▓▓            ║
╠════════════════════════════════════════════════════════════╣
║                                                            ║
║   [ 1 ]  Analyze a Password                               ║
║   [ 2 ]  Batch Scan from File                             ║
║   [ 3 ]  Generate Strong Password                         ║
║   [ 0 ]  Exit                                             ║
║                                                            ║
╚════════════════════════════════════════════════════════════╝

  root@passcrack:~#
```

---

## 👤 Author

```
Author  : Ghost Protocol
Version : 2.0
Target  : Kali Linux / VMware
Purpose : Analyze & crack-resistance test passwords
```

---

## 📄 License

This project is intended for **educational and ethical security research purposes only.**
Do not use this tool to analyze passwords you do not own or have explicit permission to test.

```
MIT License — Free to use, modify, and distribute with attribution.
```

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.

```
git checkout -b feature/your-feature
git commit -m "Add your feature"
git push origin feature/your-feature
```

---

> *"Stay ghost, operator."*
```

---

This README covers everything — features, usage, scoring logic, entropy math, batch scanning, security notes, and the full hacker aesthetic that matches your tool's vibe. Just drop it as `README.md` in the same folder as your script. Want me to also generate a `.docx` or PDF version of this?
