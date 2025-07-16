# Wireshark_Network_Traffic_Capture
Detailed Wireshark analysis of IPv6 network traffic showing TCP handshake, HTTP GET request, server response, session teardown, and multicast DNS queries. This project helps understand network protocols and traffic patterns for cybersecurity and network analysis.

# 🛰️ Network Capture Insights: IPv6 HTTP Traffic

**File Name:** v6-http.cap  
**Source:** Wireshark SampleCaptures  
**Tool Used:** Wireshark  
**Objective:** Analyze captured network traffic for patterns, protocols, and anomalies.

---

## 🔎 Packet 49 – HTTP GET Request
This packet shows a client making a standard HTTP GET request to the server’s root page ("/") using IPv6. It reflects a typical web request over HTTP/1.0, using global unicast addresses.

**Why This Matters:**  
- Understanding HTTP GET requests is key for network and web traffic analysis.  
- Shows adoption of IPv6 addressing in web communication.  
- Useful in detecting anomalies in normal browsing behavior.  

📷 Insert Image: (Frame 49 HTTP GET)  
![Packet 49 HTTP GET](images/packet-49-http-get.png)

---

## 🧾 Packet 51 – HTTP 200 OK Response
This is the server's response to Packet 49. It confirms the server delivered the requested resource correctly over HTTP/1.1.

**Details:**  
- Protocol: HTTP/1.1  
- Content-Type: text/html  
- Content Length: 23 lines of HTML  
- Port: TCP 80  
- IPv6 Addressing  

📷 Insert Image: (Frame 51 200 OK)  
![Packet 51 200 OK](images/packet-51-200-ok.png)

---

## 🌐 TCP Port 80 Filter Analysis
A full web request session was captured using the filter:  
```bash
tcp.port == 80
