# 📦 Ethical Keylogger Tool – Final Year Project 

This project is a suite of ethically designed tools developed for penetration testing purposes. It includes three key components:

- **Keylogger.exe** – Installed on the test environment (staff machine) to collect keystrokes
- **Server.exe** – Central server application to receive and store encrypted data
- **HostExt.exe** – Admin tool to retrieve and review collected data from the server

> ⚠️ **This tool is for ethical use only** in penetration testing environments with **explicit consent** from all involved parties. Misuse is strictly prohibited.
> This repo contains only the executable files to test use the tool. Stay tuned for the source codes!
---

## 🧰 Executables Overview

### 🔹 Keylogger.exe
**Purpose**: Collects keystrokes from the target machine.

**Key Features**:
- Consent-based start prompt
- AES-256 encryption of keystrokes
- Periodic upload to configured server
- Auto-cleanup of logs on shutdown
- Lightweight GUI with status and controls

**Instructions**:
1. Run `Keylogger.exe` on the client (test) machine.
2. Grant permission when prompted.
3. Configure the server IP and port if needed.
4. Press “Start Keylogger” to begin logging.
5. Press “Stop Keylogger” or close the app to end session and auto-upload logs.

> 📌 Requires Python libraries (if running from source): `pynput`, `tkinter`, `requests`, `pycryptodome`

---

### 🔹 Server.exe
**Purpose**: Acts as a local server to collect encrypted keystroke logs.

**Key Features**:
- Accepts POST requests from keylogger
- Organizes logs by device IP and folder
- Includes audit trail logging for uploads/downloads
- Built-in GUI to start/stop server, view logs, check IP

**Instructions**:
1. Launch `Server.exe` on a secured host machine.
2. Click “Start Server” to begin listening on port 5000.
3. Use the control panel to view logs or check system status.

> 🛡️ Runs on `Flask` and saves data inside a `/logs` directory.

---

### 🔹 HostExt.exe
**Purpose**: Admin retrieval and viewer tool.

**Key Features**:
- Manual or automated log download
- Save logs locally in timestamped folders
- Download summary and audit report
- Server IP configuration
- Clean and simple GUI

**Instructions**:
1. Launch `HostExt.exe` on the admin machine.
2. Enter the server IP if different.
3. Click “Download” for one-time download, or “Start Auto Download” for continuous retrieval.
4. Review logs in generated local folders.

---

## 🖥️ Platform Compatibility
- ✅ Windows 10+ (Tested)
- ⚠️ Linux/macOS not yet supported

---

## 🔐 Legal and Ethical Notice
This tool is intended **solely for use in ethical penetration testing environments**. You must have **written authorization** from the organization and individuals involved.

Violation of privacy laws such as **GDPR** or **ECPA** by using this tool unethically may result in serious legal consequences.

---

## 📄 Author Info
- 👤 **Developer**: Minindu Gunawardana  
- 🏫 **University**: University of Plymouth affiliated by NSBM Green University  
- 📧 **Contact**: dewruwanminindu@gmail.com

---

## 📚 Acknowledgements
- Supervisor: Mr. Chaminda Disanayake  
- Libraries: Python, Flask, CustomTkinter, PyCryptodome, Pynput  
- Tools tested in: VirtualBox, Windows 10 sandbox environment

