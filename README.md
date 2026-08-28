# Viberia

> Command AI agents like you're playing Civilization

Your mission control for managing AI agent teams - fully local, provider agnostic, with your own keys or existing subscriptions.

[![Apple Silicon](https://img.shields.io/badge/Download-Apple_Silicon-blue?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/get-viberia/viberia-releases/releases/download/v0.8.1/Viberia_0.8.1_aarch64.dmg)
[![Windows x64](https://img.shields.io/badge/Download-Windows_x64-blue?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTAgMGgxMS4ydjExLjJIMHpNMTIuOCAwSDI0djExLjJIMTIuOHpNMCAxMi44aDExLjJWMjRIMHpNMTIuOCAxMi44SDI0VjI0SDEyLjh6Ii8%2BPC9zdmc%2B)](https://github.com/get-viberia/viberia-releases/releases/download/v0.8.1/Viberia_0.8.1_x64-setup.exe)
[![Intel](https://img.shields.io/badge/Intel-gray?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/get-viberia/viberia-releases/releases/download/v0.8.1/Viberia_0.8.1_x64.dmg)
[![ARM64](https://img.shields.io/badge/ARM64-gray?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTAgMGgxMS4ydjExLjJIMHpNMTIuOCAwSDI0djExLjJIMTIuOHpNMCAxMi44aDExLjJWMjRIMHpNMTIuOCAxMi44SDI0VjI0SDEyLjh6Ii8%2BPC9zdmc%2B)](https://github.com/get-viberia/viberia-releases/releases/download/v0.8.1/Viberia_0.8.1_arm64-setup.exe)

[![Download v0.8.1](https://img.shields.io/badge/Download-v0.8.1-blue?style=for-the-badge)](https://github.com/get-viberia/viberia-releases/releases/tag/v0.8.1)
[![Website](https://img.shields.io/badge/Website-getviberia.com-green?style=for-the-badge)](https://getviberia.com)
[![Discord](https://img.shields.io/badge/Discord-Join-7289da?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/sDxtXn4zq7)

---

## What is Viberia?

Viberia is a desktop app for macOS and Windows that lets you orchestrate multiple AI coding agents through a strategy game-style interface. Instead of juggling terminal windows and browser tabs, you get a visual mission control where you can see every agent's status, drill into conversations, and let teams of agents coordinate automatically.

**See it in action at [getviberia.com](https://getviberia.com)**

---

## Key Features

### Visual Agent Orchestration
See all your AI agents at a glance on an interactive map. Click any agent to dive into their conversation, provide input, then zoom back out - without losing context.

### Chief of Staff HUD
A built-in AI assistant that helps you manage your workspace. Get suggested actions, route messages between agents, and monitor progress through an interactive overlay.

### Agent Teams & Buildings
Organize agents into collaborative teams. A PRD writer drafts the spec, a coder implements it, a reviewer checks the work - agents hand off to each other automatically.

### Agent Loop Scheduling
Set up recurring agent tasks on a schedule. Configure model, thinking budget, and project scope per loop.

### Multi-Provider Support
Works with Claude, ChatGPT, Gemini, and any OpenAI-compatible provider. Bring your own API keys or use your existing subscriptions.

### Local-First & Private
Everything runs on your machine. Code and conversations never leave your computer. No Viberia servers involved.

---

## Requirements

- macOS 13.0+ (Ventura or later), Apple Silicon or Intel
- Windows 10 or 11 (x64 or ARM64)
- At least one of the following coding agents installed (use the minimum version shown or newer):
  - [Claude Code](https://docs.anthropic.com/en/docs/claude-code) 2.1.119 or newer
  - [Codex CLI](https://github.com/openai/codex) 0.47.0 or newer
  - [Gemini CLI](https://github.com/google-gemini/gemini-cli) 0.43.0 or newer

> Note: Claude Code versions 2.1.74 through 2.1.117 have a known HTTP MCP bug that breaks Viberia's tool connections. Update Claude Code to 2.1.119 or newer.

---

## Install

**macOS (Apple Silicon / Intel)**

1. Download the build for your Mac:
   - **Apple Silicon (M1 or later):** [Viberia_0.8.1_aarch64.dmg](https://github.com/get-viberia/viberia-releases/releases/download/v0.8.1/Viberia_0.8.1_aarch64.dmg)
   - **Intel:** [Viberia_0.8.1_x64.dmg](https://github.com/get-viberia/viberia-releases/releases/download/v0.8.1/Viberia_0.8.1_x64.dmg)
2. Open the `.dmg` and drag Viberia to Applications
3. Right-click then Open on first launch (macOS Gatekeeper prompt)

> Not sure which Mac you have? Click the Apple menu then About This Mac. "Apple M1/M2/M3/M4" means Apple Silicon; "Intel" means the Intel build.

**Windows 10/11 (x64 or ARM64)**

1. Download the installer for your architecture:
   - **x64 (most PCs):** [Viberia_0.8.1_x64-setup.exe](https://github.com/get-viberia/viberia-releases/releases/download/v0.8.1/Viberia_0.8.1_x64-setup.exe)
   - **ARM64 (e.g. Snapdragon X / Surface Pro 11):** [Viberia_0.8.1_arm64-setup.exe](https://github.com/get-viberia/viberia-releases/releases/download/v0.8.1/Viberia_0.8.1_arm64-setup.exe)
2. Run the downloaded `.exe`. Viberia is not yet code-signed, so Windows will show a SmartScreen warning. See [Windows SmartScreen / Defender](#windows-smartscreen--defender) below for how to proceed.
3. Follow the installer prompts. Viberia launches automatically when setup completes.

> Not sure which to pick? Press `Win` + `Pause`, or go to **Settings > System > About** and check **System type**. "ARM-based processor" means ARM64; otherwise pick x64.

> Linux support coming soon.

### Windows SmartScreen / Defender

The Windows `.exe` installers above are not code-signed yet, so Windows 10/11 will warn you twice: once on download, once on launch. This is expected for new unsigned apps and does not mean the file is unsafe.

**1. During download (your browser)**

Your browser may flag the file as not commonly downloaded:

- **Microsoft Edge:** the download shows a message like "this file isn't commonly downloaded." Click the three-dot menu next to the download, then **Keep**, then on the next prompt choose **Keep anyway**.
- **Chrome:** click the overflow menu on the download bar or in the Downloads list, then **Keep**.

**2. When you run the installer**

A blue dialog titled **"Windows protected your PC"** appears:

> Microsoft Defender SmartScreen prevented an unrecognized app from starting. Running this app might put your PC at risk.

To continue:

1. Click **More info** (small link under the message text).
2. The publisher line will read **Unknown publisher** and a **Run anyway** button appears.
3. Click **Run anyway** to start the installer.

If your antivirus quarantines the download, restore it from quarantine and allow the file, then re-run.

We are working on code signing to remove these prompts in a future release.

---

## Links

- [Website](https://getviberia.com)
- [Discord](https://discord.gg/sDxtXn4zq7)
- [Release Notes](https://github.com/get-viberia/viberia-releases/releases/tag/v0.8.1)

---

## License

Proprietary. All rights reserved.
