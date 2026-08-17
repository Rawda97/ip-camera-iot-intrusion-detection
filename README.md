# Network-Based Intrusion Detection for IP Camera IoT Devices

## Project Overview

This project assesses the security of IP camera IoT environments against LAN-based attacks and develops a Network-Based Intrusion Detection System (NIDS) for detecting suspicious network behavior.

The study focuses on ONVIF-based device enumeration, RTSP communication, ARP spoofing, and network reconnaissance within a controlled and isolated laboratory environment.

The project combines network traffic analysis, custom IDS detection rules, and automated response mechanisms to improve visibility and security in IP camera deployments.

## Objectives

- Analyze security risks associated with IP camera environments and ONVIF discovery mechanisms.
- Capture and analyze network traffic during normal and attack scenarios.
- Simulate LAN-based attacks including ONVIF enumeration and ARP spoofing.
- Design and implement custom Suricata detection rules.
- Detect suspicious RTSP, ICMP, ARP, and scanning activity.
- Implement automated response mechanisms using Fail2ban and iptables.
- Evaluate the effectiveness of network-based monitoring and detection.

## Experimental Environment

The experiments were conducted in an isolated and authorized laboratory environment consisting of:

- Hikvision IP Camera
- Kali Linux attacker machine
- Client device
- Local Area Network (LAN)

## Tools and Technologies

- Kali Linux
- Wireshark
- Suricata IDS
- Nmap
- ONVIF
- RTSP
- Ettercap / Arpspoof
- Arpwatch
- Fail2ban
- iptables
- Python
- VLC

## Attack Scenarios

### 1. ONVIF Device Enumeration

ONVIF-based discovery was used to identify IP camera devices and exposed device information within the local network.

### 2. RTSP Traffic Analysis

RTSP communication was captured and analyzed using Wireshark to observe session establishment and streaming-related network activity.

### 3. ARP Spoofing

ARP spoofing was simulated to demonstrate Man-in-the-Middle positioning and traffic interception within the local network.

### 4. Network Reconnaissance

Nmap was used to identify active hosts and accessible services within the isolated laboratory network.

## Detection

Suricata was configured as a Network Intrusion Detection System (NIDS).

Custom detection rules were developed to identify suspicious network behavior associated with:

- ONVIF discovery activity
- RTSP access attempts
- ICMP probing
- Port scanning
- ARP-related anomalies

Suricata generated real-time alerts containing information such as source IP addresses, protocols, destination ports, and alert classifications.

## Automated Response

Fail2ban was integrated with Suricata alerts to provide automated temporary blocking of repeated suspicious activity.

iptables was used to enforce the resulting blocking actions.

## Results

The experiments demonstrated that LAN-based attacks against IP camera environments generate observable network indicators.

Wireshark provided packet-level visibility into normal and malicious traffic, while Suricata successfully detected multiple suspicious activities including RTSP access attempts, ICMP probing, and port scanning.

The integration of Suricata, Fail2ban, and iptables demonstrated how network monitoring can be combined with automated response mechanisms to improve the defensive capabilities of IoT surveillance environments.

## Methodology

The project followed the IMGSIE research methodology:

**Introduction → Method → Generalization → Specification → Implementation → Evaluation**

The experimental workflow included:

1. Laboratory environment setup
2. Network reconnaissance
3. ONVIF enumeration
4. RTSP traffic observation
5. ARP spoofing simulation
6. Network traffic capture and analysis
7. Suricata rule implementation
8. Automated response using Fail2ban
9. Evaluation of detection results

## Project Scope

This project focuses on LAN-based security threats targeting IP camera environments.

It does not include Internet-wide scanning, firmware exploitation, remote code execution, or destructive attacks.

All experiments were conducted in a controlled and authorized laboratory environment for educational and defensive research purposes.

## Limitations

- The experiments were conducted in a small-scale isolated LAN.
- Detection rules were customized for the experimental environment.
- The study focused primarily on LAN-based attacks.
- Encrypted traffic limits deep payload inspection.
- The project did not include firmware exploitation or advanced vulnerability assessment.

## Future Work

Future improvements may include:

- Integration with SIEM platforms such as Splunk or Microsoft Sentinel.
- Machine-learning-based anomaly detection.
- Support for additional IoT protocols.
- Automated network segmentation.
- Analysis of encrypted RTSP traffic.
- Expansion to larger enterprise surveillance environments.

## Disclaimer

This project was conducted in an isolated and authorized laboratory environment for academic, educational, and defensive cybersecurity research purposes only.
