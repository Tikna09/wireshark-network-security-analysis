# Wireshark Network Security Analysis

![Wireshark](https://img.shields.io/badge/Tool-Wireshark-blue)
![Network Security](https://img.shields.io/badge/Domain-Network%20Security-red)
![Traffic Analysis](https://img.shields.io/badge/Focus-Traffic%20Analysis-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview

**Wireshark Network Security Analysis** is a practical network-security project focused on monitoring, capturing, and analyzing network traffic using **Wireshark**.

The project combines basic network-security controls with packet-level traffic analysis. The analysis focuses on understanding normal network communication and identifying security risks associated with insecure or unencrypted protocols such as **HTTP and DNS**.

The submitted report covers firewall configuration, wireless encryption, credential security, software updates, Wireshark monitoring, HTTP analysis, DNS analysis, and security best practices.

---

## 🎯 Objectives

The main objectives of this project are to:

- Understand fundamental network-security concepts.
- Study common network threats such as viruses, worms, trojans, and phishing.
- Understand the role of the **CIA Triad** — Confidentiality, Integrity, and Availability.
- Implement basic network-security measures.
- Capture and inspect network packets using Wireshark.
- Analyze HTTP and DNS communication.
- Understand the security risks of unencrypted network traffic.
- Identify the difference between secure and insecure communication.
- Develop practical network-monitoring and security-analysis skills.

---

## 🛡️ Security Measures Studied

The project covers the following security controls:

### 1. Firewall Configuration

Windows Defender Firewall was enabled and configured to restrict unauthorized inbound connections while allowing required network communication.

The report also discusses:

- Custom inbound/outbound rules
- Port and application restrictions
- Firewall log monitoring
- Reduction of unauthorized network access

### 2. WPA2/WPA3 Encryption

Wireless-network security was studied using WPA2/WPA3 encryption concepts.

The project highlights:

- Protection of wireless communications
- Use of strong and unique passwords
- Improved protection against unauthorized access
- The role of encryption in confidentiality and integrity

### 3. Changing Default Credentials

Default administrator credentials were replaced with stronger credentials to reduce the risk of unauthorized access and automated attacks.

### 4. System and Software Updates

The project emphasizes keeping operating systems, antivirus software, routers, and applications updated to reduce exposure to known vulnerabilities.

### 5. Secure Network Configuration

Additional security practices discussed include:

- Disabling unused services and ports
- Restricting network visibility
- Using firewall and access-control rules
- Reducing the overall attack surface

---

## 🔬 Wireshark Traffic Analysis

Wireshark was used for packet-level inspection of network communication.

The captured traffic included:

- **HTTP**
- **DNS**
- **TCP**
- **HTTPS/TLS**

The analysis focused on identifying how packets move between clients, servers, and DNS resolvers.

---

## 🌐 HTTP Traffic Analysis

HTTP traffic was inspected to understand unencrypted web communication.

### Observations

- HTTP request and response headers were visible.
- Information such as host, user-agent, and content type could be observed.
- HTTP does not provide encryption for the transmitted application data.
- Plain HTTP traffic can therefore expose sensitive information to packet sniffing on an appropriately positioned network.

### Security Recommendation

Use **HTTPS** instead of HTTP whenever possible so that web communication is protected using encryption.

---

## 🔎 DNS Traffic Analysis

DNS packets were captured and analyzed to understand domain-name resolution.

The project also used **Google Public DNS (`8.8.8.8`)** to manually verify DNS resolution for `wireshark.org`.

### Observations

- DNS queries and responses were captured.
- **UDP port 53** was primarily observed for DNS communication.
- The DNS response contained IPv4 and IPv6 address information.
- The report noted initial timeout messages during the resolution test.
- The capture demonstrated the query-and-response process between the client and DNS server.

### Security Consideration

Traditional DNS traffic is not encrypted by default and can be exposed to interception or manipulation.

The report recommends considering:

- **DNS over HTTPS (DoH)**
- **DNS over TLS (DoT)**

---

## 🔐 Secure vs. Insecure Traffic

| Protocol | Typical Purpose | Encryption | Security Consideration |
|---|---|---|---|
| HTTP | Web communication | No | Traffic can be exposed to sniffing |
| DNS | Domain resolution | Traditionally no | Queries may be observable or manipulated |
| HTTPS | Secure web communication | Yes | Protects web traffic using TLS |
| TLS | Secure communication | Yes | Provides encrypted communication |

---

## 📊 Key Findings

The project identified the following important observations:

1. Network traffic can be inspected at packet level using Wireshark.
2. HTTP traffic can expose application-layer information because it is unencrypted.
3. DNS queries and responses can be observed during normal domain resolution.
4. HTTPS/TLS provides protection that plain HTTP does not.
5. Firewall configuration is an important layer of network defense.
6. Strong credentials reduce the risk of unauthorized access.
7. Regular software updates help reduce exposure to known vulnerabilities.
8. Continuous traffic monitoring can help identify unusual communication patterns.
9. Network security should use multiple defensive layers rather than relying on a single control.

---

## 🧰 Tools Used

| Tool / Technology | Purpose |
|---|---|
| **Wireshark** | Packet capture and network-traffic analysis |
| **Linux Terminal** | Network and DNS verification |
| **Windows Defender Firewall** | Host-based traffic filtering |
| **Google Public DNS** | DNS-resolution verification |
| **WPA2/WPA3** | Wireless-security concepts |

---

## 📁 Repository Structure

```text
wireshark-network-security-analysis/
│
├── README.md
│
├── Wireshark-Network-Security-Analysis-Report.pdf
│
└── screenshots/
    ├── SS01_Page02.png
    ├── SS02_Page04.png
    ├── SS03_Page04.png
    ├── SS04_Page05.png
    ├── SS05_Page05.png
    └── README.md
```

---

## 📸 Screenshots

The `screenshots/` directory contains individual images extracted from the submitted project report.

The screenshots provide visual evidence of the Wireshark traffic-analysis work, including:

- HTTP packet analysis
- DNS packet analysis
- DNS-resolution verification
- Linux terminal/network verification

---

## 📄 Project Report

The complete project documentation is available in:

**`Wireshark-Network-Security-Analysis-Report.pdf`**

The report contains the detailed theory, implementation discussion, traffic observations, security analysis, best practices, and conclusion.

---

## 🧠 Skills Demonstrated

This project demonstrates practical understanding of:

- Network traffic analysis
- Packet inspection
- Wireshark filters and packet views
- HTTP analysis
- DNS analysis
- TCP/network communication
- Network-security fundamentals
- Firewall security
- Wireless encryption concepts
- Security monitoring
- Identification of insecure protocols
- Security best practices

---

## 🔒 Ethical & Educational Use

This project is intended for **educational and authorized security-analysis purposes**.

Network traffic should only be captured and analyzed on systems and networks where you have permission to perform monitoring.

---

## 🚀 Future Improvements

Possible future extensions include:

- Analyze additional protocols such as FTP, SSH, DHCP, ARP, and ICMP.
- Create protocol-specific Wireshark display filters.
- Analyze TCP handshakes and connection termination.
- Investigate suspicious packet patterns in a controlled lab.
- Add `.pcap`/`.pcapng` capture files where appropriate and safe to share.
- Add packet statistics and protocol-distribution charts.
- Integrate Wireshark findings with an IDS such as Snort or Wazuh.
- Build a more detailed network-security monitoring workflow.

---

## ✅ Conclusion

This project provided practical experience with network-security mechanisms and packet-level traffic analysis using Wireshark.

The analysis demonstrated that effective network security requires a layered approach combining **prevention, protection, monitoring, and secure communication protocols**.

The project also showed the security importance of replacing insecure protocols such as plain HTTP and traditional unencrypted DNS with appropriately secured alternatives.

---

## 👤 Author

**Ankit Kirtane**

**Domain:** Cybersecurity / Network Security  
**Project:** Wireshark Network Security Analysis
