# Simple-port-scanner
A simple Python-based port scanner that scans a target for open TCP ports.
# 🔍 Simple Port Scanner

A simple Python-based port scanner that scans a target (IP or domain) for open TCP ports.

## ⚙️ How it works

- You enter an IP address or domain name.
- The script scans through a range of ports (you provide the start and end port).
- It checks which ports are open using the socket module.

## 📦 Requirements

- Python 3
- No external libraries needed (uses built-in `socket` and `time`)

## 🚀 Usage

Run the script:

```bash
python port.py
