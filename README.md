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


import socket
import time

print("🔍 Simple Port Scanner 🔵")
target = input("Enter the IP or domain to scan: ")
start_port = int(input("Start Port: "))
end_port = int(input("End Port: "))

print(f"\nScanning {target} from port {start_port} to {end_port}...\n")

start_time = time.time()

for port in range(start_port, end_port + 1):
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    s.settimeout(0.5)
    result = s.connect_ex((target, port))

    if result == 0:
        print(f"✅ Port {port} is OPEN")
    s.close()

end_time = time.time()
print(f"\nScan completed in {round(end_time - start_time, 2)} seconds.")


