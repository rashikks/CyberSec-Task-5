Task 5 – Capture and Analyze Network Traffic Using Wireshark


Objective

Capture live network packets and identify basic network protocols and traffic types using Wireshark.

Setup

OS: Kali Linux 

Tool: Wireshark

Interface captured: (Wi-Fi / Ethernet)




Procedure

Opened Wireshark and selected the active network interface.

Started capture and generated traffic by:

Browsing to https://example.com and a few other websites.

Running ping google.com from the terminal.

Captured traffic for ~1 minute and then stopped the capture.

Used display filters (dns, tcp, http, icmp) to analyze specific protocols.

Saved the capture file as task5_capture.pcap.


Protocols Observed

DNS (Domain Name System)

Filter: dns

Example packet:

Source IP: 192.168.*.*

Destination IP: 8.8.8.8

Description: Standard query A www.google.com

Purpose: Resolves domain names to IP addresses.

TCP (Transmission Control Protocol)

Filter: tcp

Example packet:

Source port: random high port 

Destination port: 443

Flags: SYN, ACK packets observed (three-way handshake).

Purpose: Reliable, connection-oriented transport for web and other services.

HTTP or HTTPS

Filter: http (for HTTP) or tcp.port == 443 (for HTTPS/TLS)

