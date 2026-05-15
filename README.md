# Automation-Tool

Public distribution repository for tools developed at **AI_WORKPLACE**.

This repository contains **pre-built Windows EXE files only**.
Source code is maintained in private repositories for development history tracking.

---

## Available Tools

### PacketLens
Offline analyzer for `pcap` / `pcapng` / FortiGate sniffer / tcpdump captures.
Extracts metadata that Wireshark marks as "Encrypted" (TLS 1.3 SNI/ALPN/JA4, QUIC Connection ID, HTTP/3 QPACK, DoH).

| Version | File | Size |
|---------|------|------|
| **v3.0.0** (latest) | [PacketLens-v3.0.0.exe](./PacketLens/PacketLens-v3.0.0.exe) | 46 MB |
| v2.2.0 (legacy) | [PacketLens-v2.2.0.exe](./PacketLens/PacketLens-v2.2.0.exe) | 38 MB |

**v3.0.0 highlights**: Domain Tracker (IP → domain access list), TLS 1.3 / QUIC / HTTP/3 metadata, JA4 threat fingerprint, full tab-based UI overhaul.

---

### APO (AI Policy Optimizer)
FortiGate firewall policy analyzer with severity classification and local AI analysis (Ollama hermes3).

| Version | Edition | File | Size |
|---------|---------|------|------|
| **v36** (latest) | SKBA | [APO-v36.exe](./APO/APO-v36.exe) | 35 MB |
| Public | Public | [APO-public.exe](./APO/APO-public.exe) | 34 MB |

---

### IPAM-Lite
Excel-based IP address management + concurrent gateway ping monitoring with Streamlit dashboard.

| Version | File | Size |
|---------|------|------|
| v1.0.0 | [IPAM-Lite-v1.0.0.exe](./IPAM-Lite/IPAM-Lite-v1.0.0.exe) | — |

---

### NetWatch
Network equipment status dashboard (FortiGate / Cisco / Arista / Extreme / Radware / Palo Alto / Alteon).
Concurrent ping + SSH-based ARP/interface inspection across multi-vendor environments.

| Version | File | Size |
|---------|------|------|
| v1.0.0 | [NetWatch-v1.0.0.exe](./NetWatch/NetWatch-v1.0.0.exe) | — |

---

## How to Download

Click any `.exe` filename above, then click the **Download** button on the file view page.

Direct download URL format:
```
https://github.com/yonguncho/Automation-Tool/raw/main/<Tool>/<filename>.exe
```

Example:
- https://github.com/yonguncho/Automation-Tool/raw/main/PacketLens/PacketLens-v3.0.0.exe

---

## Verification

Each tool ships as a single self-contained Windows x64 EXE — no installer, no admin rights required.

To verify integrity, compute SHA-256 in PowerShell:
```powershell
Get-FileHash .\PacketLens-v3.0.0.exe -Algorithm SHA256
```

Hashes are recorded in each tool's release notes and the corresponding blog post on https://choiceguidelab.com.

---

## License

MIT (unless noted otherwise inside the tool).

## Issues / Contact

Issues with these tools may be reported via this repository's Issues tab.
