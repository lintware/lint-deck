# 🎴 Lint Deck

**AI-powered hacking deck** — an open-source portable pentesting platform that lets Claude do the heavy lifting.

## What is this?

Lint Deck combines [OpenClaw](https://github.com/openclaw/openclaw) with portable hardware to create an autonomous pentesting rig. Point it at a target, and Claude handles tool selection, payload crafting, and attack execution.

## Hardware

- **Brain:** uConsole / Mecha Comet running OpenClaw
- **RF/HID:** Flipper Zero, Kiisu board
- **WiFi:** ESP32 / LilyGo T-Embed (WiFi Pineapple emulation)
- **Camera:** Built-in camera for visual target identification

## How it works

1. **Identify** — Camera captures the target device; Claude analyzes it
2. **Prepare** — Claude selects the right tools, installs dependencies, flashes attack modules
3. **Execute** — Automated attacks via Metasploit, custom scripts, RF replay, WiFi deauth, etc.
4. **Report** — Full findings documented automatically

## Software Stack

- **OpenClaw** — AI agent runtime (Claude as the operator)
- **Claude Shannon Skill** — Pentesting skill pack for Claude
- **Metasploit Framework** — Exploit execution
- **Aircrack-ng / WiFi tools** — Wireless attacks
- **Flipper Zero CLI** — RF, NFC, IR, BadUSB automation
- **Custom ESP32 firmware** — WiFi scanning, deauth, pineapple mode

## Vision

Traditionally, pentesting requires years of practice memorizing tools and techniques. Lint Deck democratizes offensive security by letting AI handle the tooling while you focus on strategy.

> _"Like having Iron Man's JARVIS, but for hacking."_

## Status

🚧 **Early development** — Hardware selection and skill design phase.

## Contributing

This is an open-source project by [Lintware](https://github.com/lintware). PRs and ideas welcome.

## ⚠️ Disclaimer

This tool is for **authorized security testing and educational purposes only**. Always obtain proper authorization before testing any systems you don't own. Unauthorized access to computer systems is illegal.

## License

MIT
