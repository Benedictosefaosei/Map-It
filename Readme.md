# 🗺️ MapIt – Open Any Address Instantly in Google Maps

**MapIt** is a simple Python script that lets you instantly open any location in **Google Maps** — either from your **clipboard** or from **command-line input**.  
It’s a great automation mini-project for beginners learning to work with Python’s `sys`, `webbrowser`, and `pyperclip` modules.

---

## 🚀 Features

- Opens any address directly in Google Maps from the terminal.
- Supports two modes:
  1. **Command-line mode** – Type the address directly when running the script.
  2. **Clipboard mode** – Automatically uses the address copied to your clipboard.
- Lightweight — only uses Python’s standard library and one small external module (`pyperclip`).

---

## 🛠️ Requirements

- Python 3.x
- `pyperclip` library (install via pip)

Install `pyperclip` using:

```bash
pip install pyperclip
```

📦 Installation

Clone or download this repository:

git clone https://github.com/your-username/mapit.git
cd mapit

Make sure mapit.py is inside your project folder.

▶️ Usage
🧭 Option 1: Enter address directly

You can pass the address as a command-line argument:

python mapit.py 1600 Amphitheatre Parkway, Mountain View, CA

This will automatically open:

https://www.google.com/maps/place/1600+Amphitheatre+Parkway,+Mountain+View,+CA

📋 Option 2: Use your clipboard

If you’ve copied an address to your clipboard, simply run:

python mapit.py

The script will automatically fetch the address from your clipboard and open it in Google Maps.

💡 Example
Command-line Input Example:
python mapit.py 221B Baker Street, London

👉 Opens this in your default browser:

https://www.google.com/maps/place/221B+Baker+Street,+London

Clipboard Example:

Copy: Times Square, New York

Run:

python mapit.py

Browser opens:
https://www.google.com/maps/place/Times+Square,+New+York

🧠 How It Works

The script checks if any command-line arguments were passed using sys.argv.

If arguments exist, it joins them into a full address string.

If not, it uses pyperclip to grab text from your clipboard.

Then, it constructs a Google Maps URL and opens it in your default web browser using the webbrowser module.
