<div align="center">

# Mira

### A native macOS Operating System of Agents

**You talk to one Mira. She runs a team of AI agents, tools, and your whole Mac — locally, safely, and fast.**

[![macOS](https://img.shields.io/badge/macOS-14%2B-000000?logo=apple&logoColor=white)](https://www.apple.com/macos/)
[![Apple Silicon](https://img.shields.io/badge/Apple%20Silicon-arm64-555555)](https://support.apple.com/en-us/116943)
[![Local-first](https://img.shields.io/badge/Local--first-%E2%9C%93-2ea44f)](#privacy--safety)
[![License: MIT](https://img.shields.io/badge/License-MIT-c9a227.svg)](LICENSE)

</div>

---

Mira isn't a chatbot. She's a **personal AI operating layer** for your Mac: a single, decisive interface that plans, delegates to a team of specialist agents, edits real files, drives native apps, and remembers your work — all on your machine, with every action you can review.

```bash
curl -fsSL https://github.com/jhordideamarall/mira-agent-v1/releases/latest/download/install.sh | bash
```

> This repository is the **public distribution channel** (installer + signed builds + release manifest). The source code is maintained privately.

---

## See it in action

<div align="center">

https://github.com/jhordideamarall/mira-agent-v1/raw/main/assets/memory.mp4

<sub><em>Mira's living memory graph — your work, connected, on-device.</em></sub>

</div>

|  |  |
|---|---|
| ![Chat with Mira](assets/chat-mira.png) | ![The agent team](assets/Agent-mira.png) |
| **Chat with Mira** — one decisive interface. | **The agent team** — Atlas, Lyra, Aegis & specialists. |
| ![Per-agent models](assets/Agent-mira-model.png) | ![Model connectors](assets/connector-model.png) |
| **Per-agent models** — each agent on its own model. | **Your own accounts** — Claude Code, Codex, DeepSeek. |
| ![Mind-Dump](assets/mind-dump.png) |  |
| **Mind-Dump** — speak freely; Mira structures it into memory. |  |

> If the video above doesn't play inline, [open it here](assets/memory.mp4).

---

## Why Mira

- **🧠 An orchestration layer, not a single model.** One Mira (CEO, Claude Opus 4.7) delegates to a **dynamic, token-lean agent team** — Atlas plans, Lyra builds, Aegis reviews; complex work auto-summons The Sentinel, The Chronicler, and an on-demand specialist (Security / UI / Data / Performance). Every agent is a real reasoning pass, not a script.
- **🛠️ It actually does the work — safely.** Mira writes files and operates native macOS, with every side-effecting action gated by **Plan / Accept Edits / God Mode**, an approval flow, and a hash-chained audit log. Finished tasks hand you **one-click deliverables** — open the file, the project folder, or a live preview.
- **🖥️ Operates your real Mac — natively, no cloud round-trip.** The Native Operator reads your screen (ScreenCaptureKit + on-device Vision OCR) and controls apps through Accessibility and Apple Events on *the Mac you're using* — not a remote browser or a cloud VM. Acting locally means it's faster and more direct than agents that pilot a sandbox in the cloud, and it stays under approval + audit the whole time.
- **🔑 Uses your own model accounts — no API keys.** Mira drives your installed **Claude Code** and **Codex** logins; their auth, config, and working directory carry over. **DeepSeek** joins as a first-class model.
- **🧩 Brings your setup with you.** Mira imports your existing **skills, agents, commands, and rules** from `~/.claude` and `~/.codex` — you stay in control. Per-language coding rules auto-load by project; skills and MCP servers are per-project. *Mira is the platform — no plugins to wrangle.*
- **🗺️ Local-first intelligence.** A memory graph that grows with you, a project codebase map, agentic research with cited sources, native voice, and curated frameworks per project type.

---

## Install

**Requirements**
- macOS 14 (Sonoma) or later · Apple Silicon
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) (`claude`) and [Codex](https://developers.openai.com/codex/cli/) (`codex`) installed and signed in — Mira uses your own logins, not API keys.

**One-line install**

```bash
curl -fsSL https://github.com/jhordideamarall/mira-agent-v1/releases/latest/download/install.sh | bash
```

The installer downloads the latest build, **verifies its SHA-256 checksum**, installs Mira to `/Applications`, clears the Gatekeeper quarantine, and adds a `mira` command.

---

## Update

```bash
mira update        # update to the latest published build (no-op if already current)
```

Or without the shim:

```bash
curl -fsSL https://github.com/jhordideamarall/mira-agent-v1/releases/latest/download/install.sh | bash -s -- --update
```

Other commands:

```bash
mira            # open Mira
mira version    # show the installed version
```

---

## Privacy & safety

- **Local-first.** Memory, audit log, configuration, and skills live on your Mac.
- **You only talk to Mira.** Agents never act on you directly.
- **Every side-effect is gated** — risk classification → permission mode → approval → append-only, hash-chained audit log. Read-only research tools run agentically but stay traced.
- **Secrets stay in Keychain** — never in logs, prompts, memory, or imports. Capability import never reads your tokens.

---

## Beta note

Beta builds are **self-signed** (not yet notarized by Apple), so the installer clears the Gatekeeper quarantine for you after verifying the checksum. Notarized distribution and richer auto-update are on the roadmap.

---

<div align="center">
<sub>Built for people who want their Mac to <em>do</em> things, not just chat about them.</sub>
</div>
