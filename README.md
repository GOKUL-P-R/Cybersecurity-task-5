# Cybersecurity-task-5
Hands-on Wireshark lab: capture live network traffic, filter by protocols like TCP, UDP, HTTP and DNS, export a .pcap file, and write a short report summarizing observed protocols and key packet details to build core packet analysis skills.
# Task 5 – Wireshark Packet Capture and Analysis

## 1. Environment

- Operating System: <your OS and version>
- Wireshark Version: <version you installed>
- Network Interface Used: <e.g., Wi-Fi / Ethernet>

## 2. Capture Procedure

1. Started Wireshark and selected the active network interface (e.g., Wi-Fi/Ethernet).
2. Began live capture on the selected interface.
3. Generated traffic by:
   - Browsing websites (e.g., opening a few pages in a browser).
   - Running basic network commands like `ping` or `nslookup`.
4. Stopped the capture after about one minute.
5. Saved the capture as `capture.pcap`.

## 3. Protocols Observed

### 3.1 TCP

- Purpose: Connection-oriented, reliable transport protocol in the TCP/IP suite.
- Usage observed: Used to carry web traffic and other application data.
- Example packet (from Wireshark):
  - Source IP: <src IP>
  - Destination IP: <dst IP>
  - Source Port: <src port>
  - Destination Port: <dst port>
  - Notes: <e.g., part of a web request/response>

### 3.2 UDP

- Purpose: Connectionless transport protocol, lower overhead than TCP.
- Usage observed: Used for lightweight queries such as DNS.
- Example packet:
  - Source IP: <src IP>
  - Destination IP: <dst IP>
  - Source Port: <src port>
  - Destination Port: <dst port>
  - Notes: <e.g., short request/response, no handshake>

### 3.3 DNS

- Purpose: Resolves domain names to IP addresses.
- Usage observed: Queries sent when accessing websites.
- Example packet:
  - Source IP: <client IP>
  - Destination IP: <DNS server IP>
  - Transport: UDP port 53
  - Query Name: <e.g., www.example.com>

### 3.4 (Optional) HTTP / HTTPS

- Purpose: Application-layer protocol for web communication (HTTPS over TLS for encryption).
- Usage observed: Web page loads during browsing.
- Example packet:
  - Source IP: <client IP>
  - Destination IP: <web server IP>
  - Ports: <e.g., 80 or 443>
  - Notes: <e.g., HTTP GET request, TLS handshake>

## 4. Filters Used in Wireshark

- To view only TCP packets: `tcp`
- To view only UDP packets: `udp`
- To view DNS traffic: `dns`
- To view HTTP traffic (if present): `http`

These filters helped focus on specific protocols and understand their behavior during the capture.

## 5. Key Observations

- A typical packet contains multiple layers, such as Ethernet → IP → TCP/UDP → Application protocol.
- DNS queries usually appear before web requests, as the client first resolves the domain name.
- TCP establishes connections using a handshake before data transfer, while UDP sends packets without a handshake.
- The `.pcap` file can be re-opened in Wireshark anytime for deeper analysis and screenshots.
