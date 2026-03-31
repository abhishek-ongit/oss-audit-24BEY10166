# oss-audit-24BEY10166

**Repository:** `oss-audit-24BEY10166`  
**Course:** Open Source Software (OSS NGMC) - Capstone Project  
**Student Name:** Abhishek Kumar  
**Registration Number:** 24BEY10166  
**Chosen Software:** VLC Media Player  

---

## 📖 Project Overview
This repository serves as the practical, technical component of "The Open Source Audit" capstone project. It features a suite of five Bash shell scripts designed to demonstrate practical Linux system administration, task automation, and a hands-on understanding of how open-source tools operate at the command line.

*Note: The accompanying written report—which explores the origins, licensing (GPL/LGPL), FOSS ecosystem, and ethical philosophy behind **VLC Media Player**—has been submitted separately via the VITyarthi portal.*

---

## 🛠️ Script Breakdown

Here is an overview of the 5 scripts included in this repository:

1. **`script1.sh` (System Identity Report)**  
   Acts as a dynamic welcome screen. It uses command substitution to fetch and display the Linux distribution, kernel version, current user, and system uptime, concluding with a brief note on open-source OS licensing.
   
2. **`script2.sh` (FOSS Package Inspector)**  
   Verifies whether **VLC Media Player** (alongside other key packages) is installed on the host system. It utilizes `dpkg` or `rpm` to extract the package version and employs a `case` statement to output a short philosophical note regarding the software's purpose.
   
3. **`script3.sh` (Disk and Permission Auditor)**  
   Iterates through critical system directories (e.g., `/etc`, `/var/log`, `/usr/bin`). It generates a report detailing the disk space usage, ownership, and read/write/execute permissions for each directory.
   
4. **`script4.sh` (Log File Analyzer)**  
   Reads a specified log file line-by-line using a `while-read` loop. It counts occurrences of a specific keyword (such as `ERROR` or `WARNING`) passed as a command-line argument and outputs a concise summary.
   
5. **`script5.sh` (Open Source Manifesto Generator)**  
   An interactive script that prompts the user with three questions regarding their FOSS usage and philosophy. It concatenates the responses to generate a personalized open-source manifesto, which is then saved to a local `.txt` file.

---

## ⚙️ Prerequisites & Dependencies

To execute these scripts successfully, ensure your system meets the following requirements:
* **Operating System:** A standard Linux environment (Ubuntu/Debian, CentOS/RHEL, or a compatible VM/WSL setup).
* **Target Software:** `vlc` should be installed to fully test the functionality of Script 2.
* **Package Manager:** `dpkg` (Debian/Ubuntu) or `rpm` (RedHat/CentOS) accessible in the system path.
* **GNU Utilities:** Standard tools including `awk`, `grep`, `du`, `uname`, and `uptime` (these are pre-installed on virtually all Linux distributions).

---

## 🚀 Step-by-Step Execution Guide

### Step 1: Clone the Repository
Open your Linux terminal and clone this project:
```bash
git clone https://github.com/abhishek-ongit/oss-audit-24BEY10166
```

### Step 2: Navigate to the Directory
```bash
cd oss-audit-24BEY10166
```

### Step 3: Grant Execution Permissions
Before running the scripts, you must make them executable:
```bash
chmod +x *.sh
```

### Step 4: Run the Scripts
Execute the scripts one by one using the commands below:

* **Script 1:** System Identity Report
  ```bash
  ./script1.sh
  ```
* **Script 2:** Package Inspector
  ```bash
  ./script2.sh
  ```
* **Script 3:** Disk and Permission Auditor
  ```bash
  ./script3.sh
  ```
* **Script 4:** Log File Analyzer  
  *(Note: This script requires command-line arguments: the log file path and an optional keyword. You will likely need `sudo` privileges to read system logs. If you are on CentOS/RHEL, use `/var/log/messages` instead).*
  ```bash
  sudo ./script4.sh /var/log/syslog ERROR
  ```
* **Script 5:** Manifesto Generator  
  *(Follow the interactive on-screen prompts. Once finished, check your current directory for the newly generated `.txt` file!)*
  ```bash
  ./script5.sh
  ```
