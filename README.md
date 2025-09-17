# WSL2 Arch Linux Setup

## 📊 System Information
- **OS**: Arch Linux (Version: 20250302.0.316047)
- **Kernel**: Linux 5.15.167.4-microsoft-standard-WSL2
- **Shell**: bash 5.3.3
- **Terminal**: Windows Terminal
- **Total Packages**: 252 packages installed
- **Memory**: 32GB available

## 🎨 Terminal & Prompt
### Oh My Posh
- **Version**: Custom installation
- **Theme**: `sonicboom_dark.omp.json`
- **Features**: Colorful prompt with git integration, execution time, WSL indicator
- **Location**: `/home/jhasmany/.cache/oh-my-posh/themes/`

### Blesh (Advanced Bash Enhancement)
- **Version**: 0.3.4-5
- **Features**: Syntax highlighting, advanced autocompletion
- **Toggle Command**: `bl` (activates/deactivates dynamically)
- **Optimized**: Fast configuration for responsive experience

### Fastfetch (System Info)
- **Version**: 2.52.0-1
- **Usage**: Displays system information on terminal startup
- **Shows**: OS, hardware, memory, disk usage, network info

## 🛠️ Development Environment

### Programming Languages
- **Java**: OpenJDK 21.0.8
- **Node.js**: v22.16.0 (via NVM)
- **PHP**: 8.4.12 (CLI) + PHP Legacy 8.2.29
- **Lua**: 5.4.8-2

### Development Tools
- **Git**: 2.51.0-1 with automatic SSH agent integration
- **Docker**: 28.4.0 with Docker Compose 2.39.3-1
- **Maven**: 3.9.11-1
- **Gradle**: 9.0.0-1
- **Composer**: 2.8.11-1

### Node.js Environment
- **NVM**: Installed for Node version management
- **Current Node**: v22.16.0
- **NPM**: Latest version included

### Java Environment
- **CATALINA_HOME**: Apache Tomcat configured at `/opt/tomcat`
- **Android SDK**: Configured for mobile development
  - Platform tools, emulator, build tools included
  - Path: `/mnt/c/Users/jhasm/AppData/Local/Android/Sdk`

## 🗄️ Databases
- **PostgreSQL**: 17.5-5 (Latest) + PostgreSQL 16.10-1
- **MariaDB LTS**: 11.8.3-2
- **PHP Extensions**: PDO PostgreSQL, SQLite support

## 📦 Package Management
### Pacman (Official Packages)
- **Base System**: base, base-devel, sudo
- **Development**: git, vim, docker, gradle, maven
- **Utilities**: wget, unzip, unrar, rsync, xdg-utils

### AUR (Arch User Repository)
- **AUR Helper**: yay 12.5.0-1
- **AUR Packages**: oh-my-posh, blesh, additional tools

## 🎯 Utility Tools
### File Management
- **exa**: Modern `ls` replacement with icons and colors
- **Alias**: `ls='exa --icons'`

### System Monitoring
- **gotop**: Terminal-based activity monitor
- **bpytop**: Resource monitor (Python-based)
- **gping**: Ping with graph visualization
- **Alias**: `rendimiento1='gotop'`

### Fun Terminal Tools
- **asciiquarium**: Animated aquarium in terminal
- **cmatrix**: Matrix-style terminal effect
- **sl**: Steam locomotive animation
- **Alias**: `acuario='asciiquarium'`

## 🔧 System Configuration

### SSH Configuration
- **SSH Agent**: Auto-starts when needed for git operations
- **Key**: `~/.ssh/wls-arch-linux`
- **Auto-activation**: On `git push` and `git clone`

### Bash Configuration
#### Aliases
```bash
# Package Management
alias pacman-update='sudo pacman -Syu'
alias yay-update='yay -Syu'

# Navigation (WSL Integration)
alias disk-c='cd ../../mnt/c/Users/jhasm'
alias disk-d='cd ../../mnt/d'

# File Operations
alias open='xdg-open'
alias ls='exa --icons'

# System Monitoring
alias rendimiento1='gotop'
alias acuario='asciiquarium'
```

#### Functions
- **start_ssh()**: Intelligent SSH agent management
- **git()**: Wrapper function for automatic SSH activation
- **bl()**: Toggle blesh on/off while preserving oh-my-posh

### Path Configuration
- **Local bin**: `/home/jhasmany/.local/bin`
- **Console Ninja**: `~/.console-ninja/.bin`
- **Android SDK**: Platform tools, emulator, build tools
- **Java**: Default JVM binaries
- **Tomcat**: `/opt/tomcat/bin`

## 🎨 Color & Theme Support
- **COLORTERM**: truecolor (24-bit color support)
- **Terminal Colors**: 256 color support confirmed
- **Theme Integration**: Oh-my-posh + blesh compatible setup

## 🚀 Quick Commands

### Blesh Toggle
```bash
bl          # Activate/deactivate blesh
```

### Package Updates
```bash
pacman-update    # Update system packages
yay-update       # Update AUR packages
```

### System Monitoring
```bash
rendimiento1     # Launch gotop system monitor
acuario         # Launch ASCII aquarium
```

### Development
```bash
docker --version    # Docker 28.4.0
node --version      # Node.js v22.16.0
java -version       # OpenJDK 21.0.8
php --version       # PHP 8.4.12
```

## 📁 Important Files
- **Bash Config**: `~/.bashrc` (optimized with oh-my-posh + blesh integration)
- **Blesh Config**: `~/.blerc` (minimal, performance-optimized)
- **SSH Config**: `~/.ssh/` (with WSL-specific key)
- **NVM Config**: `~/.nvm/` (Node.js version management)

## 🔄 Backup & Restore
- **Backup Created**: `~/.bashrc.backup` (before optimization)
- **Configuration Files**: All dotfiles properly configured
- **Package List**: Use `pacman -Qe` for explicit packages

---

*This WSL2 Arch Linux setup is optimized for development work with modern tooling, beautiful terminal experience, and efficient package management.*