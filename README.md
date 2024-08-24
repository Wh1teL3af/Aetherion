---

**Aetherion**: The Hyper DoS (HDoS) Tool for High-Intensity Network Stress Testing

**Overview:**
Aetherion is a state-of-the-art Hyper Denial of Service (HDoS) tool developed in Python, designed to execute high-intensity network stress tests. It simulates large-scale denial of service attacks to evaluate the robustness of network infrastructures and services. Ideal for security researchers, penetration testers, and network administrators, Aetherion provides advanced capabilities for stress testing while emphasizing ethical use.

**Core Features:**

- **TCP Flood Attack:**
  Launches a flood of valid HTTP requests to overwhelm the target’s TCP connections. The tool utilizes up to 2000 concurrent threads to maximize impact and test the target's resilience under heavy traffic conditions.

- **UDP Flood Attack:**
  Sends a high volume of UDP packets to the target, potentially causing network congestion and service interruptions. This feature is effective against services relying on UDP for communication.

- **ICMP Flood Attack:**
  Sends a flood of ICMP packets to the target, targeting the network layer to cause potential outages and connectivity issues.

**Advanced Capabilities:**

- **High-Concurrency Execution:**
  Aetherion supports up to 2000 concurrent threads for each attack vector, ensuring realistic stress testing with significant impact.

- **Safety and Monitoring:**
  Includes safety warnings about system overload risks and monitors request counts to manage attack intensity.

**Usage Guidelines:**

- **Ethical and Authorized Use Only:**
  Aetherion is for educational purposes, authorized network stress testing, and security research. Unauthorized use is illegal and unethical. Ensure you have explicit permission before conducting any tests.

- **System Overload Warning:**
  Due to its high-concurrency nature, Aetherion can strain systems, especially local machines. Be cautious and ensure that your testing environment can handle the load.

**How to Use:**

1. **Installation:**
   Clone the repository and install any required dependencies listed in the `requirements.txt` file:
   ```
   git clone https://github.com/yourusername/aetherion.git
   cd aetherion
   pip install -r requirements.txt
   ```

2. **Running the Tool:**
   You can initiate attacks using the following commands. Make sure to replace `<IP>` with the target IP address and `<PORT>` with the target port number if applicable.

   - **TCP Flood Attack:**
     ```
     python main.py flood --ip <IP> --port <PORT>
     ```
     Initiates a TCP flood attack with valid HTTP requests.

   - **UDP Flood Attack:**
     ```
     python main.py udp-flood --ip <IP> --port <PORT>
     ```
     Launches a UDP flood attack.

   - **ICMP Flood Attack:**
     ```
     python main.py icmp-flood --ip <IP>
     ```
     Deploys an ICMP flood attack.

3. **Command Details:**

   - **flood**
     - **Description:** Initiate a targeted TCP Flood attack.
     - **Options:**
       - `--ip`: Target IP address (Required).
       - `--port`: Target port (default: 80).

   - **udp-flood**
     - **Description:** Launch a UDP Flood attack on the target.
     - **Options:**
       - `--ip`: Target IP address (Required).
       - `--port`: Target port (default: 80).

   - **icmp-flood**
     - **Description:** Deploy an ICMP Flood attack.
     - **Options:**
       - `--ip`: Target IP address (Required).

4. **Help Menu:**
   To view the help menu with usage instructions and options, run:
   ```
   python main.py --help
   ```

**Disclaimer:**
The developers of Aetherion are not liable for any damages or legal consequences resulting from misuse. Ensure compliance with applicable laws and regulations. Misuse of Aetherion can result in serious legal repercussions.

**Contributions and Support:**
Aetherion is an open-source project, and contributions are encouraged. For bug reports, feature requests, or support, please refer to the repository’s issue tracker and documentation.

---
