# My-Projects


## 🧪 Static Malware Analysis Process

1. 🗂 **File Type Identification**

   * Use `HxD`, `file`, or `TrID` to check file type (`.exe`, `.dll`, etc.).
   * Look for the `MZ (4D 5A)` header in PE files.

2. 🔐 **Hash Calculation & Reputation Check**

   * Generate hashes using `HashMyFiles` or `Hashcalc`.
   * Upload to [VirusTotal](https://www.virustotal.com) for detection reports.

3. 🧵 **Strings Extraction**

   * Run the `strings` command to find embedded data like IPs, URLs, or commands.
   * Use `XORSearch` to identify and decode obfuscated strings.

4. 📦 **Packer Detection**

   * Analyze the file with tools like **DIE**, **PEStudio**, or **PEiD**.
   * Packed files often show unusual section names (e.g., `.upx`, `.aspack`).

5. 🔍 **PE Header Inspection**

   * Use `PE-bear` or `PEView` to inspect section headers, imports, and metadata.
   * Check for suspicious or missing sections.

---

## 💣 Dynamic Malware Analysis Process

1. 🖥️ **Isolated Lab Setup**

   * Deploy **FlareVM** and **Remnux** in **VirtualBox** with Host-Only networking.
   * Ensure the lab is air-gapped (no internet access).

2. 🌐 **Network Simulation**

   * Route FlareVM traffic through **INetSim** on Remnux to simulate internet services.
   * Capture and analyze traffic using **Wireshark**.

3. 🔎 **Process & System Monitoring**

   * Use `ProcMon` and `Process Hacker` to track file system, registry, and process activity.
   * Look for anomalies like unexpected processes or file writes.

4. 📁 **Behavior Analysis**

   * Observe dropped files, created folders, registry keys, and persistence methods.
   * Check for signs of privilege escalation or command-and-control (C2) communication.

5. 🧠 **Memory Analysis (Optional)**

   * Capture memory dumps and analyze with **Volatility** to find injected code, hidden DLLs, or malicious threads.


