# 🎴 Lint Deck

**AI-powered pentesting toolkit on portable hardware** — Claude as your operator, Flipper Zero as your hands.

![Status](https://img.shields.io/badge/status-early%20development-yellow)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-uConsole%20%7C%20Mecha%20Comet-lightgrey)

## What is this?

Lint Deck is an open-source portable pentesting platform that combines [OpenClaw](https://github.com/openclaw/openclaw) (AI agent runtime) with handheld hardware. Point it at a target — Claude handles reconnaissance, tool selection, payload crafting, and attack execution autonomously.

> _"Like having JARVIS, but for hacking."_

## Architecture

```
┌─────────────────────────────────────────────┐
│            Lint Deck (Portable)              │
│                                             │
│  ┌─────────────┐    ┌──────────────────┐    │
│  │  OpenClaw   │◄──►│  Claude (Opus/   │    │
│  │  Runtime    │    │  Sonnet)         │    │
│  └──────┬──────┘    └──────────────────┘    │
│         │                                   │
│  ┌──────┴──────────────────────────────┐    │
│  │         Tool Orchestration          │    │
│  ├─────────┬──────────┬────────────────┤    │
│  │         │          │                │    │
│  ▼         ▼          ▼                ▼    │
│ 📡        📻        📶              🎯    │
│ Flipper   ESP32     WiFi            Camera  │
│ Zero      Module    Tools           (CV)    │
│ RF/NFC/   Pineapple Aircrack-ng     Target  │
│ IR/BadUSB emulation Metasploit      ID      │
└─────────────────────────────────────────────┘
```

## Hardware

| Component | Device | Role |
|-----------|--------|------|
| **Brain** | uConsole / Mecha Comet | Runs OpenClaw + Claude |
| **RF/HID** | Flipper Zero, Kiisu board | Sub-GHz, NFC, IR, BadUSB |
| **WiFi** | ESP32 / LilyGo T-Embed | WiFi scanning, deauth, evil twin |
| **Camera** | Built-in / USB | Visual target identification |

## How It Works

1. **🔍 Identify** — Camera captures the target; Claude analyzes the device type, ports, and attack surface
2. **🧰 Prepare** — Claude selects the right tools, installs dependencies, configures attack modules
3. **⚡ Execute** — Automated attacks via Metasploit, RF replay, WiFi deauth, BadUSB payloads, etc.
4. **📝 Report** — Full findings documented automatically with evidence and remediation steps

## Software Stack

| Tool | Purpose |
|------|---------|
| [OpenClaw](https://github.com/openclaw/openclaw) | AI agent runtime — Claude as the operator |
| Claude Shannon Skill | Pentesting skill pack (recon, exploit, report) |
| Metasploit Framework | Exploit development and execution |
| Aircrack-ng | WiFi auditing and WPA cracking |
| Flipper Zero CLI | RF, NFC, IR, BadUSB automation |
| Custom ESP32 firmware | WiFi scanning, deauth, pineapple mode |
| Nmap / Masscan | Network discovery and port scanning |

## Vision

Pentesting traditionally requires years memorizing tools, flags, and techniques. Lint Deck flips the model: **AI handles the tooling, you handle the strategy.** Tell Claude what you want to test — it figures out the how.

Use cases:
- **Red team engagements** — Portable rig for physical + wireless assessments
- **CTF competitions** — AI-assisted flag hunting
- **Security education** — Learn offensive security with an AI tutor explaining each step
- **IoT auditing** — Quick assessments of smart devices, BLE peripherals, RF remotes

## Status

🚧 **Early development** — Hardware selection and skill design phase.

### Roadmap

- [ ] Core OpenClaw skill for pentesting workflows
- [ ] Flipper Zero CLI integration
- [ ] ESP32 WiFi module firmware
- [ ] Camera-based target identification
- [ ] Metasploit session management
- [ ] Report generation templates
- [ ] uConsole build guide
- [ ] Mecha Comet build guide

## Contributing

This is an open-source project by [Lintware](https://github.com/lintware). PRs, ideas, and hardware suggestions welcome.

## ⚠️ Disclaimer

This tool is for **authorized security testing and educational purposes only.** Always obtain proper written authorization before testing any systems you don't own. Unauthorized access to computer systems is illegal under the Computer Fraud and Abuse Act (CFAA) and equivalent laws worldwide.

The authors are not responsible for any misuse of this software.

## License

MIT

---

Built with 🔥 by [Lintware](https://github.com/lintware)
