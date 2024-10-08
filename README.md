# Network Traffic Analysis Tool - Project Overview
This project is a **Network Traffic Analysis Tool** developed using **Python** on **Kali Linux**. The tool captures network traffic, analyzes it for potential security threats, and provides real-time visualization of the traffic patterns. Below are the key components and functionalities of the project:

## Project Setup
* Clone the repository and navigate to the project directory:

```bash
git clone <repository_link>
cd network_traffic_analysis_tool
```
* Set up a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

* Install the necessary Python dependencies:

```bash
pip install scapy pandas plotly
```
## Running the Tool
* To run the tool, use the following command:

```bash
sudo python3 network_traffic_analysis.py
```
This command will start the tool, asking you to input the network interface you wish to monitor (e.g., **eth0**, **wlan0**).

* After entering the interface, the tool will begin packet sniffing and capture traffic in real-time, analyzing each packet for potential security threats, such as malicious IPs.

## Key Functionalities
* **Real-time Threat Detection:** The tool analyzes incoming packets and flags any traffic from a malicious IP. You will see warnings in the terminal if such IPs are detected.

* **Traffic Visualization:** After capturing a specified number of packets, the tool prompts:

```bash
Do you want to visualize the captured traffic? (y/n):
```
Selecting **‘y’** will generate a graph displaying the packet count per source IP. This graph helps identify any unusual traffic or potential Distributed Denial-of-Service (DDoS) attempts.

## Adding Duration to Packet Capture
The tool also supports specifying a duration for packet capture. You can modify the **duration** variable to control how long the tool captures traffic.

## Python's Role in the Project
Python plays a central role in this project by leveraging various libraries:

**Scapy:** Used for capturing and analyzing network packets.

**Pandas:** For organizing and manipulating packet data.

**Plotly:** For visualizing the network traffic patterns in an interactive graph.
Python was chosen due to its vast library support for network traffic analysis, ease of use, and ability to handle both data analysis and visualization in a single ecosystem.

## How to Use the Tool
### 1. Start the Tool:
Run the script with **sudo python3 network_traffic_analysis.py** and specify the network interface (e.g., **eth0**).

### 2. Monitor Packets:
The tool will display packets in real-time, flagging any malicious IPs detected.

### 3. Visualize Traffic:
After the packet capture, the tool will prompt for visualization. Type **y** to display the traffic patterns in a bar chart.

## Advantages
* Real-time threat detection using predefined malicious IPs.
* Visual representation of traffic to easily spot abnormalities.
* Python-based solution using libraries like Scapy, Pandas, and Plotly.

## Future Enhancements
* Integrating a threat intelligence feed to dynamically update the list of malicious IPs.
* Adding more advanced traffic filtering options to focus on specific protocols or types of packets.
* Automating periodic reports for network administrators with the traffic analysis results.

## References

- **Scapy**: Used for packet sniffing and network traffic analysis. Documentation can be found [here](https://scapy.net/doc/).
- **Pandas**: For data manipulation and processing. Check out the documentation [here](https://pandas.pydata.org/).
- **Plotly**: For creating interactive data visualizations. Learn more [here](https://plotly.com/python/).
- **Kali Linux**: The operating system used for network traffic analysis. You can explore more [here](https://www.kali.org/).
