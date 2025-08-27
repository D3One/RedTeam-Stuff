# RedTeam-Stuff 🔴⚔️

A collection of custom scripts, tools, and utilities crafted during my hands-on penetration testing engagements. This repository serves as my public arsenal for red team operations, automation, and research.

**Disclaimer:**
> These tools are provided for **educational and authorized testing purposes only**. Never use them on any system without explicit, written permission. Unauthorized access to computer systems is illegal and unethical. The author is not responsible for any misuse or damage caused by this software.

<p align="center">
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/50146ee8-ede0-445a-af2f-7cf059724893" />
</p>

---

## Tools Overview

### 1. `anomaly-scanner.nse` - Nmap Anomaly Detection Script

A custom Nmap Scripting Engine (NSE) script designed to augment traditional port scanning by hunting for indicators of anomalous or potentially malicious activity on a target host.

*   **Purpose:** Goes beyond simple service discovery to flag behaviors often associated with compromised systems, security monitoring, or non-standard configurations.
*   **Key Features:** The script checks for:
    *   Unexpected open ports commonly used by malware or backdoors.
    *   Signs of port knocking sequences.
    *   Services running on non-standard ports.
    *   TCP/IP stack anomalies that could indicate evasion or filtering.
*   **Usage:** `nmap --script ./anomaly-scanner.nse <target>`
*   **For a detailed explanation of checks and output,** please refer to the comments within the script file itself.

### 2. `express-pentest.py` - Kali Linux Express PenTest Script

A Python wrapper script designed to automate the initial stages of a penetration test. It sequentially runs a curated set of powerful tools from the Kali Linux arsenal to perform a rapid, baseline assessment of a target.

*   **Purpose:** To save time and ensure consistency during the initial reconnaissance and vulnerability discovery phases of an engagement. It's a great starting point for beginners to learn the workflow.
*   **Workflow:** The script automates the execution of tools for:
    *   **DNS Enumeration** (e.g., using `dnsrecon`, `dig`)
    *   **Port Scanning** (e.g., with `nmap` and its scripting engine)
    *   **Directory Bruteforcing** (e.g., with `gobuster` or `dirb`)
    *   **Basic Vulnerability Scanning** (e.g., with `nikto`)
*   **Usage:** `python3 express-pentest.py -t <target>`
*   **Note:** This is a **framework and a starting point**. The specific tools and commands are detailed in the script's comments. You are expected to customize the command arguments and tool selection based on your target and goals.

---

<p align="center">
  <img src="https://github.com/user-attachments/assets/9f93298e-0016-45e2-b241-8feabc60fec4" />
</p>

## Getting Started

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/D3One/RedTeam-Stuff.git
    cd RedTeam-Stuff
    ```

2.  **Review the Code:** Before running any script, always inspect the code to understand what it does.
3.  **Install Dependencies:** Ensure you have the required tools installed (e.g., `nmap`, `python3`, `nikto`, `gobuster`). A standard Kali Linux installation will have most of them.
4.  **Run with Permission:** Only execute these scripts on targets you are explicitly authorized to test.

---

## Contributing

Found a bug, have an idea for a new feature, or want to add your own custom tool?
Contributions are welcome! Feel free to fork the repository, make your changes, and submit a Pull Request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingTool`)
3.  Commit your Changes (`git commit -m 'Add some AmazingTool'`)
4.  Push to the Branch (`git push origin feature/AmazingTool`)
5.  Open a Pull Request

---

## License

This project is licensed under the MIT License. This means you can use the code for any purpose, including commercial projects, as long as you include the original license and disclaimer. See the `LICENSE` file for details.
> "We must be free not because we claim freedom, but because we practice it.” — William Faulkner

Any future work done must follow the guidelines mentioned in GPLv3.0.

---

*This repository is a testament to the principle of "Automate Everything." Happy (authorized) hacking!*
