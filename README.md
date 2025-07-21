
🔐 Cybersecurity Tools Assignment

This repository contains five basic cybersecurity tools written in Python and Bash, covering port scanning, host discovery, and NSE script automation with Nmap.
📁 Contents

    Port Scanner without Nmap (Python)

    Port Scanner using nmap module (Python)

    Overview of nmap Python Module

    Host Discovery Tool (Python)

    Nmap NSE Script Tool (Bash)

1. Port Scanner without Nmap (Python)

File: simple_port_scanner.py
This tool uses Python's built-in socket module to scan the first 1024 ports on a given IP address.

python3 simple_port_scanner.py

Features:

    No third-party modules required

    Scans TCP ports from 1 to 1024

    Identifies open ports

2. Port Scanner using Nmap Module (Python)

File: nmap_port_scanner.py
This tool uses the python-nmap wrapper to scan open ports on a target IP.
Requirements:

Install the python-nmap module:

pip install python-nmap

Usage:

python3 nmap_port_scanner.py

Features:

    Scans ports 1-1024

    Displays service status of each open port

3. Overview of Nmap Python Module

python-nmap is a wrapper around the Nmap CLI tool, allowing integration of Nmap scans into Python scripts.
Key Methods:

    scan(hosts, ports) — Runs the scan

    all_hosts() — Lists all discovered hosts

    Access results like:
    scanner[host]['tcp'][port]['state']

    Useful for writing automation scripts in penetration testing.

4. Host Discovery Tool (Python)

File: host_discovery.py
This tool determines the default gateway IP address and its IP class (A, B, or C).
Usage:

python3 host_discovery.py

Features:

    Detects the default gateway (Linux only)

    Classifies IP address based on the first octet

5. Nmap NSE Script Tool (Bash)

File: nse_scan.sh
A Bash script that accepts a target IP and an NSE script name to run a custom Nmap scan.
Usage:

chmod +x nse_scan.sh
./nse_scan.sh <IP_ADDRESS> <NSE_SCRIPT_NAME>

Example:

./nse_scan.sh 192.168.1.1 http-enum

Features:

    Simplifies running advanced NSE-based scans

    Useful for penetration testing automation

💡 Notes

    All Python scripts are for educational use and run on Linux systems.

    Use sudo where required (e.g., for Nmap).

    Ensure Nmap is installed on your system:

    sudo apt install nmap

📚 License

This project is for academic and educational purposes only.


