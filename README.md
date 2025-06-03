# MCDP CLI

A powerful command-line interface for Monotone Co-Design Problems (MCDP) operations.

## 🖥️ Platform Support

| Operating System | Architecture  | Status       |
|------------------|---------------|--------------|
| Ubuntu 22        | x86_64, ARM64 | ✅ Supported |
| Ubuntu 24        | x86_64, ARM64 | ✅ Supported |
| macOS 15         | Intel, Apple Silicon | ✅ Supported |
| Windows 11       | x86_64, ARM64 | 🧪 Experimental |

## 📋 Prerequisites

- **Docker** - A working Docker installation is required
  - [Install Docker Desktop](https://www.docker.com/products/docker-desktop/) (Windows/macOS)
  - [Install Docker Engine](https://docs.docker.com/engine/install/) (Linux)

## 🚀 Installation

### Quick Install

Download the appropriate binary for your system from the [latest releases](https://github.com/zupermind/mcdp-binaries/releases/latest).

### Platform-Specific Instructions

<details>
<summary><b>🐧 Linux (Ubuntu)</b></summary>

1. Download the binary for your architecture
2. Make it executable:
   ```bash
   chmod +x mcdp-cli-*
   ```
3. (Optional) Move to system path:
   ```bash
   sudo mv mcdp-cli-* /usr/local/bin/mcdp
   ```
4. Verify installation:
   ```bash
   mcdp version
   ```

</details>

<details>
<summary><b>🍎 macOS</b></summary>

**⚠️ Security Notice:** Browsers may quarantine downloaded executables. Use the command line to avoid security warnings.

#### Recommended Installation (via Terminal):

```bash
# For Apple Silicon Macs (M1/M2/M3)
curl -L -o mcdp https://github.com/zupermind/mcdp-binaries/releases/latest/download/mcdp-cli-[VERSION]-macos15-arm64

# For Intel Macs
curl -L -o mcdp https://github.com/zupermind/mcdp-binaries/releases/latest/download/mcdp-cli-[VERSION]-macos15-amd64

# Make executable
chmod +x mcdp

# Verify installation
./mcdp version

# (Optional) Move to system path
sudo mv mcdp /usr/local/bin/
```

Replace `[VERSION]` with the actual version number from the releases page.

</details>

<details>
<summary><b>🪟 Windows (Experimental)</b></summary>

**⚠️ Note:** Windows support is currently experimental. Please report any issues you encounter.

#### Native Windows (PowerShell/Command Prompt)

1. Download the `.exe` file for your architecture
2. **If downloaded via browser:** You may see security warnings - click "More info" → "Run anyway"

#### Recommended Installation (via PowerShell):

```powershell
# For x64
curl -L -o mcdp.exe https://github.com/zupermind/mcdp-binaries/releases/latest/download/mcdp-cli-[VERSION]-windows-amd64.exe

# For ARM64
curl -L -o mcdp.exe https://github.com/zupermind/mcdp-binaries/releases/latest/download/mcdp-cli-[VERSION]-windows-arm64.exe

# Verify installation
.\mcdp.exe version
```

#### Windows Subsystem for Linux (WSL)

If using WSL, download the **Ubuntu** version instead and follow the Linux instructions.

**💡 Tip:** This is a CLI tool. If you double-click the .exe file, you'll see instructions on how to use it from a terminal.

</details>

## 🔄 Updating

The MCDP CLI includes a built-in self-update feature:

```bash
mcdp-cli update
```

This command will:
- Check for the latest version
- Download and install it automatically
- Preserve your current settings

## 🎯 Getting Started

Once installed, you can:

```bash
# View help and available commands
mcdp help

# Check version
mcdp version
```

## 📚 Documentation

For detailed usage instructions and examples, visit our [documentation](https://docs.mcdp.org).

## 🐛 Troubleshooting

<details>
<summary><b>Common Issues</b></summary>

### "Command not found" error
- Ensure the binary is in your system PATH or use the full path to the executable

### Permission denied (Linux/macOS)
- Run `chmod +x mcdp` to make the file executable

### Security warnings (Windows/macOS)
- Use the command-line installation method to avoid browser quarantine
- On Windows, you may need to add an exception in Windows Defender

### Docker not found
- Ensure Docker is installed and running
- On Linux, you may need to add your user to the docker group: `sudo usermod -aG docker $USER`

</details>

## 🤝 Support

- 🐛 [Report Issues](https://github.com/zupermind/releases/issues)
