# 🛡️ Kali Linux Complete Setup Script

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Prerequisites](#-prerequisites)
- [Quick Start](#-quick-start)
- [Installed Tools](#-installed-tools)
- [Directory Structure](#-directory-structure)
- [Post-Installation](#-post-installation)
- [Fish Shell Features](#-fish-shell-features)
- [Usage Examples](#-usage-examples)
- [Updating Tools](#-updating-tools)
- [Troubleshooting](#-troubleshooting)

---

## 🎯 Overview

This comprehensive automated setup script transforms a fresh Kali Linux installation into a fully-configured penetration testing powerhouse. Designed for security professionals, bug bounty hunters, and red team operators, it eliminates hours of manual configuration and ensures consistent, reproducible environments.

### Why This Script?

- ⏰ **Save 4-6 hours** of manual installation time
- 🎯 **42 essential tools** carefully selected and organized
- 🐚 **Modern shell experience** with Fish + Starship
- 📊 **Organized workflow** with categorized tool directories
- 🔄 **Easy updates** with built-in update functions
- 📝 **Comprehensive logging** for troubleshooting
- ✅ **Production-tested** and battle-hardened

---

## ✨ Features

### 🔧 Core Components

<table>
<tr>
<td width="50%">

**Development Environment**
- ✅ Go 1.21+ (latest)
- ✅ Rust toolchain (via rustup)
- ✅ Python 3.11+ with pipx
- ✅ Docker & Docker Compose
- ✅ OpenJDK 21 LTS

</td>
<td width="50%">

**Shell Environment**
- ✅ Fish shell with custom config
- ✅ Starship prompt (nerd-font preset)
- ✅ Eza (modern ls replacement)
- ✅ Modern CLI tools (bat, fd, ripgrep)
- ✅ Custom functions & abbreviations

</td>
</tr>
</table>

### 🛠️ Tool Categories

| Category | Tools | Description |
|----------|-------|-------------|
| 🌐 **Web** | 10 tools | Web application security testing |
| 🔍 **Recon** | 7 tools | Reconnaissance and enumeration |
| 🕸️ **Network** | 4 tools | Network analysis and pivoting |
| 🔓 **Exploit** | 2 tools | Exploitation frameworks and C2 |
| 🩸 **AD** | 5 tools | Active Directory assessment |
| 🔐 **PrivEsc** | 2 tools | Privilege escalation |
| 🤖 **Automation** | 2 tools | Automated reconnaissance |
| 🔍 **OSINT** | 3 tools | Information gathering |
| ☁️ **Cloud** | 2 tools | Cloud security testing |
| 🔧 **Misc** | 5 tools | Various utilities |

### 🎨 Script Features

- 🎨 **Colorful output** with progress indicators
- 📊 **Real-time progress** (1/200, 2/200...)
- 📝 **Detailed logging** to `~/kali-setup.log`
- ⚠️ **Smart error handling** (continues on non-critical errors)
- 🔐 **Optional certificate installation**
- ⏱️ **Performance metrics** (installation time tracking)
- 📈 **Comprehensive summary** at completion
- 🔄 **Idempotent design** (safe to re-run)

---

## 🔧 Prerequisites

### System Requirements

- **OS:** Kali Linux 2024.1 or newer
- **RAM:** 4GB minimum (8GB recommended)
- **Disk Space:** 20GB free space
- **Internet:** Stable internet connection
- **Privileges:** Root or sudo access

### Recommended

- Fresh Kali Linux installation
- Updated system packages
- Backup of important data

---

## 🚀 Quick Start

### One-Line Installation

```bash
# Download and run the script
curl -fsSL https://raw.githubusercontent.com/barispekalp/kali-setup/main/kali-setup.sh | sudo bash
```

### Manual Installation

```bash
# Clone the repository
git clone https://github.com/barispekalp/kali-setup.git
cd kali-setup

# Make script executable
chmod +x kali-setup.sh

# Run the script
sudo ./kali-setup.sh
```

### With Custom Certificate

```bash
# Run with your organization's certificate
sudo ./kali-setup.sh /path/to/your/certificate.crt
```

### Installation Time

```
⏱️ Estimated time: 60-90 minutes
📊 Total steps: 200+
🔧 Tools installed: 42
📚 Wordlist repos: 3
```

---

## 🛠️ Installed Tools

### 🌐 Web Application Security (10 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **ffuf** | Go | Fast web fuzzer |
| **httpx** | Go | HTTP probing toolkit |
| **katana** | Go | Web crawling framework |
| **nuclei** | Go | Vulnerability scanner |
| **dalfox** | Go | XSS scanner |
| **feroxbuster** | Rust | Directory bruteforcer |
| **XSStrike** | Python | Advanced XSS detection |
| **Arjun** | Python | HTTP parameter discovery |
| **Corsy** | Python | CORS misconfiguration scanner |
| **sqlmap** | Python | SQL injection tool |

</details>

### 🔍 Reconnaissance & Enumeration (7 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **subfinder** | Go | Subdomain discovery |
| **assetfinder** | Go | Domain finder |
| **amass** | Go | DNS enumeration |
| **puredns** | Go | DNS bruteforcing |
| **dnsx** | Go | DNS toolkit |
| **naabu** | Go | Port scanner |
| **rustscan** | Rust | Ultra-fast port scanner |

</details>

### 🕸️ Network Analysis & Pivoting (4 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **chisel** | Go | HTTP tunneling |
| **ligolo-ng** | Go | Advanced tunneling (proxy + agent) |
| **rustcat** | Rust | Netcat alternative |

</details>

### 🔓 Exploitation & C2 (2 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **sliver** | Go | Modern C2 framework |
| **impacket** | Python | SMB/MSRPC toolkit |

</details>

### 🩸 Active Directory (5 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **Neo4j** | Database | Graph database for BloodHound |
| **BloodHound** | JavaScript | AD analysis GUI |
| **RustHound** | Rust | BloodHound data collector |
| **Certipy** | Python | AD certificate abuse |
| **Coercer** | Python | Force Windows authentication |

</details>

### 🔐 Privilege Escalation (2 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **PEASS-ng** | Bash/C# | Privilege escalation suite |
| **linux-exploit-suggester** | Bash | Kernel exploit suggester |

</details>

### 🤖 Automation Frameworks (2 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **AutoRecon** | Python | Multi-threaded reconnaissance |
| **ReconFTW** | Bash | Automated recon framework |

</details>

### 🔍 OSINT (3 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **sherlock** | Python | Social media username search |
| **holehe** | Python | Email OSINT |
| **h8mail** | Python | Email breach hunting |

</details>

### ☁️ Cloud & Container Security (2 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **trivy** | Go | Container vulnerability scanner |
| **kube-hunter** | Python | Kubernetes pentesting |

</details>

### 🔧 Miscellaneous (2 tools)

<details>
<summary>Click to expand</summary>

| Tool | Type | Description |
|------|------|-------------|
| **Ciphey** | Python | Automated decryption |
| **haiti** | Ruby | Hash identifier |

</details>

### 📚 Wordlist Repositories (3 repos)

- **fuzzdb** - Comprehensive fuzzing patterns
- **SecLists** - Industry-standard wordlists
- **PayloadsAllTheThings** - Practical payload collection

---

## 📁 Directory Structure

```
~/
├── wordlists/                    # Wordlist repositories
│   ├── fuzzdb/
│   ├── SecLists/
│   └── PayloadsAllTheThings/
│
├── pentests/                     # Project organization
│   ├── 2026.01/
│   ├── 2026.02/
│   └── ... (all months)
│
└── tools/                        # Categorized tools
    ├── web/                      # Web application security
    │   ├── XSStrike/
    │   ├── Arjun/
    │   ├── Corsy/
    │   └── sqlmap/
    ├── recon/                    # Reconnaissance
    ├── network/                  # Network analysis
    ├── exploit/                  # Exploitation
    │   └── sliver/
    ├── ad/                       # Active Directory
    │   ├── BloodHound/
    │   └── Coercer/
    ├── privesc/                  # Privilege escalation
    │   ├── PEASS-ng/
    │   └── linux-exploit-suggester/
    ├── automation/               # Automation
    │   └── reconftw/
    ├── osint/                    # OSINT
    │   └── holehe/
    ├── cloud/                    # Cloud security
    │   ├── trivy/
    │   └── kube-hunter/
    └── misc/                     # Miscellaneous
```

---

## 🔄 Post-Installation

### 1️⃣ Restart Your Session

```bash
# Log out and log back in for all changes to take effect
logout
```

This activates:
- New shell (Fish)
- Docker group membership
- PATH changes
- Environment variables

### 2️⃣ Configure API Keys

#### Subfinder

```bash
nano ~/.config/subfinder/provider-config.yaml
```

Example configuration:

```yaml
virustotal:
  - YOUR_VT_API_KEY
shodan:
  - YOUR_SHODAN_API_KEY
censys:
  - YOUR_CENSYS_API_ID:YOUR_CENSYS_API_SECRET
binaryedge:
  - YOUR_BINARYEDGE_API_KEY
bevigil:
  - YOUR_BEVIGIL_API_KEY
```

[Get API Keys →](https://github.com/projectdiscovery/subfinder#post-installation-instructions)

#### Amass

```bash
nano ~/.config/amass/config.ini
```

Example configuration:

```ini
[data_sources]
[data_sources.AlienVault]
[data_sources.AlienVault.Credentials]
apikey = YOUR_ALIENVAULT_API_KEY

[data_sources.BinaryEdge]
[data_sources.BinaryEdge.Credentials]
apikey = YOUR_BINARYEDGE_API_KEY

[data_sources.Censys]
[data_sources.Censys.Credentials]
apikey = YOUR_CENSYS_API_ID
secret = YOUR_CENSYS_API_SECRET
```

[Get API Keys →](https://github.com/owasp-amass/amass/blob/master/examples/config.ini)

### 3️⃣ Setup Neo4j for BloodHound

```bash
# Start Neo4j service
sudo systemctl start neo4j
sudo systemctl enable neo4j

# Access Neo4j web interface
firefox http://localhost:7474
```

**Default credentials:**
- Username: `neo4j`
- Password: `neo4j`

⚠️ **Important:** Change password on first login!

### 4️⃣ Build Required Tools

Some tools require manual building:

#### Sliver C2 Framework

```bash
cd ~/tools/exploit/sliver
make
```

#### Trivy Scanner

```bash
cd ~/tools/cloud/trivy
go install
```

#### Kube-hunter

```bash
cd ~/tools/cloud/kube-hunter
pip install -r requirements.txt --break-system-packages
```

### 5️⃣ Verify Installation

```bash
# Test Go tools
httpx -version
nuclei -version
subfinder -version

# Test Rust tools
feroxbuster --version
rustscan --version

# Test Python tools
impacket-smbclient --help
certipy --help

# Test navigation
toolsweb    # Should navigate to ~/tools/web
```

---

## 🐚 Fish Shell Features

### 🎨 Custom Functions

#### System Management

```fish
update-system          # Update system packages
update-wordlists       # Update wordlist repositories
update-tools           # Update all pentesting tools
venv                   # Activate Python virtual environment
```

#### Quick Navigation

```fish
toolsweb              # cd ~/tools/web
toolsrecon            # cd ~/tools/recon
toolsnetwork          # cd ~/tools/network
toolsexploit          # cd ~/tools/exploit
toolsad               # cd ~/tools/ad
toolsprivesc          # cd ~/tools/privesc
toolsauto             # cd ~/tools/automation
toolsosint            # cd ~/tools/osint
toolscloud            # cd ~/tools/cloud
toolsmisc             # cd ~/tools/misc
```

### ⚡ Abbreviations

The script installs powerful abbreviations that expand as you type:

#### File Operations

```fish
ll        # eza -la --icons --group-directories-first
la        # eza -a --icons --group-directories-first
..        # cd ..
...       # cd ../..
....      # cd ../../..
```

#### Git Shortcuts

```fish
gst       # git status
gco       # git checkout
gp        # git pull
gps       # git push
ga        # git add
gc        # git commit
gd        # git diff
gl        # git log --oneline --graph
```

#### Docker Shortcuts

```fish
dps       # docker ps
dpsa      # docker ps -a
di        # docker images
dex       # docker exec -it
dlog      # docker logs -f
```

---

## 💡 Usage Examples

### Web Application Testing

```bash
# Subdomain enumeration
subfinder -d target.com | httpx -mc 200

# Directory fuzzing
ffuf -u https://target.com/FUZZ -w ~/wordlists/SecLists/Discovery/Web-Content/raft-large-directories.txt

# Vulnerability scanning
nuclei -u https://target.com -t ~/nuclei-templates/
```

### Reconnaissance

```bash
# Fast port scan
rustscan -a target.com -- -sV -sC

# DNS enumeration
dnsx -l subdomains.txt -resp

# Active subdomain verification
cat subdomains.txt | httpx -title -tech-detect -status-code
```

### Active Directory

```bash
# Collect BloodHound data
rusthound -d domain.local -u user -p password -o bloodhound

# Certificate abuse
certipy find -u user@domain.local -p password -dc-ip 10.10.10.10

# SMB enumeration
impacket-smbclient domain/user:password@target
```

### Automation

```bash
# Automated reconnaissance
autorecon target.com

# Comprehensive recon
cd ~/tools/automation/reconftw
./reconftw.sh -d target.com -a
```

---

## 🔄 Updating Tools

### Quick Update

```fish
# Update everything
update-system && update-tools && update-wordlists
```

### Individual Updates

```fish
# Update system packages
update-system

# Update pentesting tools
update-tools

# Update wordlists
update-wordlists
```

### Manual Updates

```bash
# Update specific Go tool
go install github.com/ffuf/ffuf/v2@latest

# Update specific Rust tool
cargo install feroxbuster

# Update all pipx tools
pipx upgrade-all

# Update git repositories
cd ~/tools/web/sqlmap && git pull
```

---

## 🐛 Troubleshooting

### Common Issues

<details>
<summary><b>"Command not found" after installation</b></summary>

**Solution:**
```bash
# Restart your session
logout

# Or reload PATH
source ~/.cargo/env
```

</details>

<details>
<summary><b>Docker permission denied</b></summary>

**Solution:**
```bash
# Restart session to activate docker group
logout

# Or use newgrp
newgrp docker
```

</details>

<details>
<summary><b>Go tools not found</b></summary>

**Solution:**
```bash
# Check GOPATH
echo $GOPATH  # Should be ~/go

# Add to PATH manually
set -gx PATH $PATH $HOME/go/bin
```

</details>

<details>
<summary><b>Nuclei templates update fails</b></summary>

**Solution:**
```bash
# Manual update
nuclei -update-templates

# Or reinstall
go install github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
nuclei -update-templates
```

</details>

<details>
<summary><b>Fish shell not default after installation</b></summary>

**Solution:**
```bash
# Change shell manually
chsh -s /usr/bin/fish

# Verify
echo $SHELL  # Should be /usr/bin/fish
```

</details>

### Log Analysis

Check the installation log for detailed error messages:

```bash
# View entire log
cat ~/kali-setup.log

# Find errors
grep ERROR ~/kali-setup.log

# Find warnings
grep WARNING ~/kali-setup.log

# Last 50 lines
tail -50 ~/kali-setup.log
```
