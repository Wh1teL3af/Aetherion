### Aetherion: The Hyper DoS (HDoS) Tool for High-Intensity Network Stress Testing

#### -- WhiteLeaf

## Overview
Aetherion is a cutting-edge Hyper Denial of Service (HDoS) tool developed in Python, designed for high-intensity network stress testing. It simulates large-scale denial of service attacks to assess the robustness of network infrastructures and services. This tool is ideal for security researchers, penetration testers, and network administrators who need to perform advanced stress testing, while emphasizing ethical use.

![image](https://github.com/user-attachments/assets/e4c53ce0-07c9-4428-ae2e-4060e09d3b72)


## Core Features
- **TCP Flood Attack:** Floods the target’s TCP connections with a high volume of valid HTTP requests. Utilizes up to 2000 concurrent threads to maximize impact and test resilience.
- **UDP Flood Attack:** Sends a large volume of UDP packets to the target, causing potential network congestion and service interruptions.
- **ICMP Flood Attack:** Sends a flood of ICMP packets to the target, impacting network layer services and causing potential outages.

## Advanced Capabilities
- **High-Concurrency Execution:** Supports up to 2000 concurrent threads per attack vector for comprehensive stress testing.
- **Safety and Monitoring:** Includes safety warnings for system overload risks and monitors request counts to manage attack intensity.

## Usage Guidelines
- **Ethical and Authorized Use Only:** Aetherion is intended for educational purposes, authorized stress testing, and security research. Unauthorized use is illegal and unethical. Always obtain explicit permission before conducting any tests.
- **System Overload Warning:** Due to high concurrency, Aetherion may strain systems, especially local machines. Ensure your testing environment can handle the load.

## How to Use

### Installation
Clone the repository and install the required dependencies:
```bash
git clone https://github.com/yourusername/aetherion.git
cd aetherion
pip install -r requirements.txt
```

### Running the Tool
You can initiate attacks using the following commands. Replace `<IP>` with the target IP address and `<PORT>` with the target port number if applicable.

- **TCP Flood Attack:**
  ```bash
  python main.py flood --ip <IP> --port <PORT>
  ```
  Initiates a TCP flood attack with valid HTTP requests.

- **UDP Flood Attack:**
  ```bash
  python main.py udp-flood --ip <IP> --port <PORT>
  ```
  Launches a UDP flood attack.

- **ICMP Flood Attack:**
  ```bash
  python main.py icmp-flood --ip <IP>
  ```
  Deploys an ICMP flood attack.

### Command Details

- **flood**
  - **Description:** Initiates a targeted TCP Flood attack.
  - **Options:**
    - `--ip`: Target IP address (Required).
    - `--port`: Target port (default: 80).

- **udp-flood**
  - **Description:** Launches a UDP Flood attack on the target.
  - **Options:**
    - `--ip`: Target IP address (Required).
    - `--port`: Target port (default: 80).

- **icmp-flood**
  - **Description:** Deploys an ICMP Flood attack.
  - **Options:**
    - `--ip`: Target IP address (Required).

### Help Menu
To view the help menu with usage instructions and options, run:
```bash
python main.py --help
```

## Disclaimer
The developer (me) of Aetherion are not liable for any damages or legal consequences resulting from misuse. Ensure compliance with all applicable laws and regulations. Misuse of Aetherion can lead to serious legal repercussions.

## Contributions and Support
Aetherion is an open-source project, and contributions are welcome! For bug reports, feature requests, or support, please use the repository’s issue tracker and documentation.
