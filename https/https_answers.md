## https analysis
## 7. What is the name of website?
- Website Name : example.com

## 8. Find the packet that contains the ClientHello message for the website you are accessing.
- Packet No : 9
- Time : 0.339124

## 9.  List all the TLS extensions included in the ClientHello.
The ClientHello included the following TLS extensions:
- Extensions Length: 1657
- Extension: Reserved (GREASE) (len=0)
- Extension: supported_groups (len=12)
- Extension: renegotiation_info (len=1)
- Extension: compress_certificate (len=3)
- Extension: key_share (len=1263) X25519MLKEM768, x25519
- Extension: ec_point_formats (len=2)
- Extension: encrypted_client_hello (len=218)
- Extension: application_layer_protocol_negotiation (len=14)
- Extension: psk_key_exchange_modes (len=2)
- Extension: server_name (len=34) name=clientservices.googleapis.com
- Extension: supported_versions (len=7) TLS 1.3, TLS 1.2
- Extension: status_request (len=5)
- Extension: session_ticket (len=0)
- Extension: signed_certificate_timestamp (len=0)
- Extension: extended_master_secret (len=0)
- Extension: Unknown type 17613 (len=5)
- Extension: signature_algorithms (len=18)
- Extension: Reserved (GREASE) (len=1)

## 10. Identify the ServerHello message. What cipher suite is chosen by the server? 
- Packet No : 12
- Time : 0.520741
- Cipher Suite: TLS_CHACHA20_POLY1305_SHA256 (0x1303)

## 11.  Locate the Certificate message. Extract the server’s certificate information (issuer, subject, validity dates).

# Issuer:
- CN = DigiCert Global G3 TLS ECC SHA384 2020 CA1
- O = DigiCert Inc
- C = US 
# subject:
- CN = *.example.com
- O = Internet Corporation for Assigned Names and Numbers
- L = Los Angeles
- ST = California
- C = US
# validity:
- Not Before, Not after

## 12.  After the TLS handshake, identify the first encrypted application data packet. Why can’t you directly see the HTTP headers in this packet? 

- Packet No : 911 contains first Application Data.
- Transport Layer Security
    TLSv1.2 Record Layer: Application Data Protocol: Hypertext Transfer Protocol

