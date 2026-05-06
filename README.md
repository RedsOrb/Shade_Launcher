<div align="center">
  <img src="icon.png" alt="Shade Launcher" width="200" />

  # Shade Launcher

  **The modern Minecraft launcher built for power users.**

  Reproducible profiles · Deduplicated storage · Blazing fast

  <br />

  <p align="center">
    <a href="https://github.com/RedsOrb/Shade_Launcher/releases/latest"><img src="https://img.shields.io/github/v/release/RedsOrb/Shade_Launcher?style=for-the-badge&color=white&labelColor=0a0a10&label=Download" alt="Latest Release"></a>
    <img src="https://img.shields.io/github/license/RedsOrb/Shade_Launcher?style=for-the-badge&color=white&labelColor=0a0a10" alt="MIT License">
    <img src="https://img.shields.io/github/stars/RedsOrb/Shade_Launcher?style=for-the-badge&color=white&labelColor=0a0a10" alt="Stars">
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust">
    <img src="https://img.shields.io/badge/Tauri-24C8D8?style=for-the-badge&logo=tauri&logoColor=white" alt="Tauri">
    <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React">
  </p>

  <p align="center">
    <a href="#-download">Download</a> ·
    <a href="#-features">Features</a> ·
    <a href="#-why-shade">Why Shade?</a> ·
    <a href="#-architecture">Architecture</a>
  </p>

  <br />

</div>

<br />

---

<br />

## 📥 Download

Get the latest version of Shade Launcher:

<div align="center">

| Platform | Download | Format |
|:---:|:---:|:---:|
| 🪟 **Windows** | [**Download Installer**](https://github.com/RedsOrb/Shade_Launcher/releases/latest) | `.exe` setup |
</div>

> 🌐 **Or visit our website:** [shadelauncher.web.app](https://shadelauncher.web.app) for a one-click download.

<br />

---

<br />

## ✨ Features

<table>
<tr>
<td width="50%">

### 📦 Deduplicated Storage
Install the same mod across 10 profiles — it's stored **once**. SHA-256 content-addressed store means zero wasted disk space.

</td>
<td width="50%">

### 📜 Declarative Profiles
Your setup is a single JSON file. Version control it, share with friends, diff changes, and restore anytime.

</td>
</tr>
<tr>
<td width="50%">

### ⚡ Blazing Fast
Built in Rust with Tauri. Near-instant startup, parallel downloads, and minimal memory footprint.

</td>
<td width="50%">

### 🌐 Modrinth + CurseForge
Search and install mods, resource packs, and shaders from both platforms directly in the launcher.

</td>
</tr>
<tr>
<td width="50%">

### 🔒 Private & Secure
Zero telemetry. No launcher account required. Your data stays local. Works perfectly offline.

</td>
<td width="50%">

### ⚙️ All Mod Loaders
Fabric, Forge, Quilt, NeoForge — with automatic version resolution and dependency management.

</td>
</tr>
<tr>
<td width="50%">

### 👤 Multi-Account
Switch between Microsoft accounts instantly with secure, encrypted token storage.

</td>
<td width="50%">

### 🕵️ No Hidden State
Plain JSON on disk. Predictable directory layout. Fully inspectable — no magic, no mystery.

</td>
</tr>
</table>

<br />

---

<br />

## 💡 Why Shade?

Most launchers come with bloat, telemetry, and opaque state. Shade takes a different approach:

> **Your game setup is code.** Declarative, reproducible, and efficient.

- **One library, infinite profiles** — Content-addressed deduplication means mods are shared, not copied
- **Profiles are portable** — Plain JSON files you can git-commit, share, or restore
- **Nothing hidden** — Every file is inspectable, every directory is predictable
- **Built for speed** — Rust backend with parallel I/O, no Electron overhead
- **Your data is yours** — No accounts, no tracking, no cloud sync you didn't ask for

<br />

---

<br />

## 🏗️ Architecture

| Principle | How it works |
|:---|:---|
| **Single source of truth** | Profiles are JSON manifests. Instances are derived, regenerated on demand. |
| **Deduplication** | SHA-256 content-addressed store. One file, infinite profiles. |
| **Transparency** | Plain JSON on disk. Predictable layout. Fully inspectable state. |
| **Modular** | Auth, Minecraft data, and profiles are isolated and swappable. |

<br />

### 📂 Data Layout

```
~/.shade/
├── store/                    # Content-addressed storage
│   ├── mods/sha256/
│   ├── resourcepacks/sha256/
│   └── shaderpacks/sha256/
├── profiles/                 # Profile manifests
│   └── <id>/profile.json
├── instances/                # Materialized game directories
├── minecraft/                # Versions, libraries, assets
├── accounts.json             # Encrypted account tokens
└── config.json               # Launcher settings
```

<br />

---

<br />

## 🛡️ Tech Stack

| Layer | Technology |
|:---|:---|
| **Backend** | Rust |
| **Framework** | Tauri v2 |
| **Frontend** | React + TypeScript |
| **Storage** | SHA-256 content-addressed filesystem |
| **Auth** | Microsoft OAuth (MSAL) |
| **APIs** | Modrinth API, CurseForge API |

<br />

---

<br />

## 📄 License

Shade Launcher is open-source software licensed under the [MIT License](LICENSE).

<br />

---

<div align="center">
  <br />
  <img src="icon.png" alt="Shade" width="48" />
  <br /><br />
  <b>Shade Launcher</b>
  <br />
  <sub>Built with ❤️ in Rust</sub>
  <br /><br />
  <a href="https://github.com/RedsOrb/Shade_Launcher">GitHub</a> ·
  <a href="https://github.com/RedsOrb/Shade_Launcher/releases">Releases</a> ·
  <a href="https://github.com/RedsOrb/Shade_Launcher/issues">Report Bug</a>
</div>
