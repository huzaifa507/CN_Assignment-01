## quic analysis
## 1. What is the name of website?
- Website Name :  www.youtube.com
## 2. Find the packet that contains the Initial QUIC handshake. What information is exchanged here? 
- Packet No: 10
- Time : 0.136638
  # Info: 
- QUIC IETF
- QUIC Connection information
- [Packet Length: 1250]
- 1... .... = Header Form: Long Header (1)
- .1.. .... = Fixed Bit: True
- ..00 .... = Packet Type: Initial (0)
- [.... 00.. = Reserved: 0]
- [.... ..00 = Packet Number Length: 1 bytes (0)]
- Version: 1 (0x00000001)
- Destination Connection ID Length: 8
- Destination Connection ID: 9a56c0d92db8bc0c
- Source Connection ID Length: 0
- Token Length: 0
- Length: 1232
## 3. Identify the QUIC packet that contains the TLS ClientHello (QUIC embeds TLS handshake inside QUIC).
- Packet No : 10
- Path: QUIC → CRYPTO → TLSv1.3 Handshake → Client Hello
## 4. Which QUIC version is used in your trace? 
- Packet NO : 10 
- Version: 1 (0x00000001)
## 5. Locate the packet where 0-RTT or 1-RTT keys are first used? 
- First Short Header packet (encrypted with 1-RTT keys).
- Wireshark may not label it, but by definition all Short Header packets use 1-RTT encryption.
## 6. Find the first packet that carries application data (HTTP/3). How does this differ from HTTP over TCP?
- Packet : 11 
- Time : 0.136865
## Difference
- QUIC runs on UDP instead of TCP.
- TLS 1.3 encryption is built directly into QUIC.
- Multiplexing streams avoids head-of-line blocking.
- Faster connection setup is possible (0-RTT / 1-RTT).
 
