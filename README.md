## 💡 Why Opreker? (The "Scratch Your Own Itch" Story)

Modern SSH clients have become massive suites. Tools like Termius and MobaXterm are great, but they often feel heavily bloated, consume too much RAM, or constantly push cloud-sync features. 

Worst of all? Many lack a simple, local backup option, effectively forcing you into vendor lock-in and cloud dependency.

**When it comes to server credentials, your keys should never leave your machine.** Opreker was built to be the exact opposite:
1. **Insanely Lightweight:** Compiles down to a ~15MB native binary.
2. **100% Local Privacy:** No accounts, no mandatory cloud sync, zero telemetry.
3. **Your Data, Your Control:** Features a seamless, AES-256-GCM encrypted local backup & import system.

## ✨ Key Features

- 🛡️ **Privacy First & Native Security:** Passwords and SSH keys are securely locked directly inside your macOS Keychain.
- 📦 **The Anti-Cloud Lock-in (Encrypted Backups):** Easily switch Macs or backup your configs locally. 1-click exports are fully encrypted via AES-256-GCM.
- ⚡ **Zero-Lag Context Switching:** Multi-session SSH with persistent terminal buffers. Your sessions don't disconnect or clear when switching tabs.
- 📁 **Seamless Dual-Pane SFTP:** Local and remote file browser implemented via shell commands over SSH for maximum server compatibility.
- 🔑 **Authentication Support:** Full support for password and SSH Key authentication (including passphrase support).
- 📊 **Real-time Metrics:** Native file transfer progress indicators.

## 🛠️ Under the Hood (Tech Stack)

Opreker is a ~4,800 LOC project (1.6k Rust / 3k TS) built around performance and developer experience:

- **Core & Backend:** [Rust](https://www.rust-lang.org/) + [Tauri](https://tauri.app/)
- **SSH Implementation:** `russh` (pure Rust async SSH client)
- **Session Management:** Actor-based SSH session management using `Tokio` channels for non-blocking IO.
- **Frontend:** React 18 + TypeScript + Tailwind CSS
- **Terminal Emulation:** `xterm.js` (Instances remain mounted in the DOM to preserve buffer state effortlessly).

## 🚀 Installation

*Note: Currently optimized for macOS (Apple Silicon).*

**Download the latest release:**
1. Go to the [Releases]([https://github.com/USERNAME/opreker/releases](https://github.com/OprekerSejati/Opreker-SSH-Manager/releases/tag/0.0.1)) page.
2. Download the `.dmg` file.
3. Drag and drop `Opreker` into your Applications folder.
