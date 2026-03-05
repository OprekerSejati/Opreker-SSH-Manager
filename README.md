# Opreker-SSH-Manager
Modern SSH and SFTP Manager

# Opreker SSH Manager

A lightweight, fast, native SSH & SFTP client built with **Rust + Tauri + React**.

After trying tools like Termius and MobaXterm, I wanted something simpler, faster, and fully under my control.  
So I built my own.

Opreker SSH Manager is a desktop SSH client focused on **speed, minimalism, and security**, while still providing the features developers actually need.

Currently supports **macOS (Apple Silicon)**.

---

## ✨ Features

### Multi-session SSH
Connect to multiple servers simultaneously with independent terminal tabs.

### Persistent Terminal Buffers
Terminal instances stay mounted when switching tabs, preserving scrollback history and session state.

### Dual-Pane SFTP Browser
Side-by-side **local and remote file explorer** for quick file transfer.

### Secure Credential Storage
Passwords are stored in **macOS Keychain**, never in plain text.

### Encrypted Backup
Connection data can be exported/imported using:

- AES-256-GCM encryption
- PBKDF2 key derivation

### SSH Key Authentication
Supports SSH private keys with **passphrase protection**.

### Real-Time File Transfers
Transfer progress is displayed in real time.

---

## 🧠 Technical Highlights

**Backend**

- Rust
- Tauri framework
- `russh` (pure Rust async SSH client)
- Tokio async runtime
- Actor-based session management via channels

**Frontend**

- React 18
- TypeScript
- xterm.js
- Tailwind CSS

Architecture decisions:

- **Actor pattern** for SSH session management
- Terminal instances remain mounted using **CSS visibility toggling**
- SFTP implemented via **shell commands over SSH** instead of the SFTP subsystem for maximum server compatibility

---

