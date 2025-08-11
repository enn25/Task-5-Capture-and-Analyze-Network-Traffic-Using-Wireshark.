# Task 5 : Capture and Analyze Network Traffic Using Wireshark.

## Objective
Capture live network packets and identify basic protocols and traffic types.

---

## Steps Performed

1. **Installed Wireshark**  
   Downloaded and installed Wireshark from the official website. Ensured that packet capture drivers (Npcap for Windows / libpcap for Linux) were installed.

2. **Started Capturing on Active Network Interface**  
   Opened Wireshark and selected the active network interface (`enp0s3`) for packet capture.

3. **Generated Network Traffic**  
   - Opened multiple websites in the browser.  
   - Performed `ping` commands to generate ICMP traffic.

4. **Stopped Capture After 1 Minute**  
   Captured network traffic for approximately 1 minute and then stopped recording.

5. **Filtered Captured Packets by Protocol**  
   Used Wireshark's display filters to isolate specific protocols:
   - **DNS**: `dns`
   - **HTTP**: `http`
   - **TCP**: `tcp`
   - **QUIC**: `quic`

6. **Identified at Least 3 Different Protocols**  
   From the capture, the following protocols were identified:
   - **DNS** – Resolving domain names to IP addresses.
   - **HTTP** – Unencrypted web requests and responses.
   - **TCP** – Transmission Control Protocol for reliable communication.
   - **QUIC** – UDP-based protocol for fast, encrypted communication (often used by Google services).

7. **Exported the Capture as `.pcap` File**  
   Saved the capture as `capture.pcap` for submission.

8. **Summarized Findings and Packet Details**  

   ### **Protocol 1: DNS**
   - Standard query and response packets.
   - Example: Query for `fonts.googleapis.com` and responses containing IP addresses.

   <img width="1000" height="900" alt="dns" src="https://github.com/user-attachments/assets/d5123bb1-2580-4786-a29c-2d9c7b431715" />

   ### **Protocol 2: HTTP**
   - Example GET request to `detectportal.firefox.com`.
   - Shows request headers like User-Agent, Accept-Language, etc.

   <img width="1000" height="900" alt="http" src="https://github.com/user-attachments/assets/c2cdef99-ec72-49bb-9bd8-cda0644bf434" />

   ### **Protocol 3: TCP**
   - TCP handshake and data transfer.
   - Example packet showing SYN, ACK, and data transfer for HTTP traffic.

   <img width="1000" height="900" alt="tcp" src="https://github.com/user-attachments/assets/43ccee65-abc1-4051-b807-d84eed9f5fd3" />

   ### **Protocol 4: QUIC**
   - Encrypted data transfer, often used for HTTPS via UDP.
   - Example packet contains Initial and Handshake frames.

   <img width="1000" height="900" alt="quic" src="https://github.com/user-attachments/assets/ca0c9ee8-e978-44c6-bb79-8a86b6f11c77" />

   ### **Example Packet Details**
   - Captured an HTTP GET request with headers for `success.txt` file.
   - Included source and destination IP addresses, protocol stack, and payload bytes.

   <img width="1918" height="970" alt="packet_details" src="https://github.com/user-attachments/assets/6e9a0636-6806-4ebd-b19f-9892535a13b7" />

---

## Summary of Key Learnings
- Learned how to capture and analyze live network packets.
- Understood the differences between DNS, HTTP, TCP, and QUIC.
- Practiced using display filters to focus on specific protocol traffic.
- Gained insight into how protocols interact in typical web browsing.

---

**Files Included in Repository**:
- `capture.pcap` – Raw packet capture.
- `README.md` – This documentation.
- Screenshots: `dns.png`, `http.png`, `tcp.png`, `quic.png`, `packet_details.png`.
