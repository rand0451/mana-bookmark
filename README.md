# 🔖 MANA

<div align="center">

![MANA Logo]([https://via.placeholder.com/200x200/667eea/ffffff?text=MANA](https://github.com/rand0451/mana-bookmark/blob/main/icon/256x256.png?raw=true))

**A powerful, modern desktop bookmark manager with real-time synchronization**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-2.1.0-brightgreen.svg)](https://github.com/yourusername/mana/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey.svg)](https://github.com/yourusername/mana/releases)
[![Electron](https://img.shields.io/badge/Electron-28.0-47848F.svg)](https://www.electronjs.org/)

[Download](https://github.com/yourusername/mana/releases) • [Documentation](docs/) • [Report Bug](https://github.com/yourusername/mana/issues) • [Request Feature](https://github.com/yourusername/mana/issues)

</div>

---

## ✨ Features

### 🎯 Core Features
- **📁 Multi-Source Management** - Monitor folders with HTML bookmark files from any browser
- **🔄 Real-Time Sync** - Automatic detection and synchronization of bookmark file changes
- **🎨 Beautiful Interface** - Modern, dark-themed UI with smooth animations and glassmorphism design
- **⚡ Lightning Fast** - Optimized performance with virtual scrolling and lazy loading
- **🔍 Smart Search** - Instant search across all bookmarks with folder filtering
- **✏️ Full Editing** - Edit titles, URLs, folders, create new bookmarks and folders
- **📊 Statistics** - Real-time statistics dashboard with folder breakdown

### 🚀 Performance Optimizations
- **Virtual Scrolling** - Render only visible bookmarks for minimal RAM usage
- **Lazy Loading** - Load favicons on-demand as they enter viewport
- **File-Level Filtering** - Toggle individual bookmark files to reduce memory footprint
- **Smart Caching** - LRU cache for favicons with configurable limits (max 500 entries)
- **Pagination** - Configurable items per page (25-200)
- **Memory Management** - Automatic cleanup of DOM fragments and observers

### 🎛️ Advanced Features
- **Multi-Browser Support** - Works with Chrome, Firefox, Edge, Safari bookmark exports
- **Folder Hierarchy** - Preserved folder structure from original bookmark files
- **Batch Operations** - Select multiple bookmarks for bulk actions
- **Keyboard Shortcuts** - `Ctrl+K` for search, `Ctrl+1/2` for file switching
- **Cross-Platform** - Native builds for Windows, macOS, and Linux
- **Portable Mode** - Run without installation on Windows

---

## 📸 Screenshots

<div align="center">

### Main Interface
![Main Interface](https://via.placeholder.com/800x500/1a1a2e/667eea?text=Main+Interface)

### Search & Filter
![Search](https://via.placeholder.com/800x500/1a1a2e/764ba2?text=Search+%26+Filter)

### Settings Panel
![Settings](https://via.placeholder.com/800x500/1a1a2e/f77062?text=Settings)

</div>

---

## 🚀 Getting Started

### Prerequisites
- Windows 10/11, macOS 10.13+, or Linux (Ubuntu 18.04+, Fedora 30+)
- No additional dependencies required

### Installation

#### Windows
1. Download `MANA-v2.1.0.zip` from [Releases](https://github.com/yourusername/mana/releases)
2. Extract the archive
3. Run `MANA.exe` (portable, no installation needed)

**Alternative:** Download `MANA-Setup.exe` for system-wide installation

#### macOS
1. Download `MANA-v2.1.0.dmg` from [Releases](https://github.com/yourusername/mana/releases)
2. Open the DMG file
3. Drag MANA to Applications folder
4. Launch from Applications

#### Linux
**AppImage (Universal):**
```bash
wget https://github.com/yourusername/mana/releases/download/v2.1.0/MANA-v2.1.0.AppImage
chmod +x MANA-v2.1.0.AppImage
./MANA-v2.1.0.AppImage
```

**Debian/Ubuntu (.deb):**
```bash
wget https://github.com/yourusername/mana/releases/download/v2.1.0/MANA-v2.1.0.deb
sudo dpkg -i MANA-v2.1.0.deb
```

**Snap:**
```bash
snap install mana
```

---

## 📖 How to Use

### Step 1: Export Your Bookmarks

**Chrome/Edge:**
1. Open browser
2. Press `Ctrl+Shift+O` → Bookmarks Manager
3. Click ⋮ (three dots) → Export bookmarks
4. Save as `bookmarks.html`

**Firefox:**
1. Press `Ctrl+Shift+B` → Library
2. Import and Backup → Export Bookmarks to HTML
3. Save file

**Safari:**
1. File → Export Bookmarks
2. Save as `Safari Bookmarks.html`

### Step 2: Configure MANA
1. Launch MANA
2. Click **Change Folder**
3. Select folder containing your exported bookmark files
4. MANA automatically detects and merges all HTML files

### Step 3: Manage Your Bookmarks
- **Search:** Use top search bar or press `Ctrl+K`
- **Filter by File:** Toggle individual files in sidebar
- **Edit:** Click edit icon on any bookmark card
- **Delete:** Click trash icon
- **Add New:** Click `+ Add Bookmark` button
- **Change View:** Toggle between grid and list views

---

## ⚙️ Configuration

### Performance Settings
Access via Settings button (⚙️ icon):

| Setting | Description | Recommended |
|---------|-------------|-------------|
| **Virtual Scroll** | Render only visible items | ✅ On |
| **Lazy Load** | Load favicons on-demand | ✅ On |
| **Favicon Cache** | Cache favicons in memory | ✅ On |
| **Memory Management** | Auto-cleanup unused resources | ✅ On |
| **Items Per Page** | Pagination size | 50-100 |

### File Filtering
- Toggle individual files on/off in **SOURCE FILES** section
- Click 👁️ icon to show/hide all files
- Disabled files are hidden but remain synchronized

---

## 🏗️ Building from Source

### Requirements
- Node.js 18+ and npm
- Git

### Clone & Install
```bash
git clone https://github.com/yourusername/mana.git
cd mana
npm install
```

### Run Development Mode
```bash
npm run dev
```

### Build for Production

**Windows:**
```bash
npm run build:windows
# Output: dist/MANA-v2.1.0.zip (Portable)
# Output: dist/MANA-Setup.exe (Installer)
```

**macOS:**
```bash
npm run build:mac
# Output: dist/MANA-v2.1.0.dmg
# Output: dist/MANA-v2.1.0.zip
```

**Linux:**
```bash
npm run build:linux
# Output: dist/MANA-v2.1.0.AppImage
# Output: dist/MANA-v2.1.0.deb
# Output: dist/MANA-v2.1.0.snap
```

---

## 🛠️ Technology Stack

- **Framework:** [Electron](https://www.electronjs.org/) 28.0
- **File Watching:** [Chokidar](https://github.com/paulmillr/chokidar) 3.5.3
- **HTML Parsing:** [node-html-parser](https://github.com/taoqf/node-html-parser) 6.1.12
- **Build System:** [electron-builder](https://www.electron.build/) 26.4.0
- **UI:** Pure HTML5/CSS3/JavaScript (No frameworks)

---

## 📊 Performance Metrics

| Metric | Value |
|--------|-------|
| **App Size (Portable)** | 93.7 MB |
| **RAM Usage (1000 bookmarks)** | ~80 MB |
| **RAM Usage (5000 bookmarks)** | ~120 MB |
| **Cold Start Time** | < 2 seconds |
| **Search Speed (1000 items)** | < 50ms |
| **File Sync Latency** | < 100ms |

---

## 🗺️ Roadmap

### v2.2.0 (Planned)
- [ ] Export bookmarks to JSON/CSV
- [ ] Import from browser profiles directly
- [ ] Duplicate detection
- [ ] Broken link checker
- [ ] Tag system

### v2.3.0 (Future)
- [ ] Cloud sync (Google Drive, Dropbox, OneDrive)
- [ ] Browser extensions for live sync
- [ ] Mobile apps (iOS/Android)
- [ ] Bookmark sharing & collaboration
- [ ] AI-powered bookmark organization

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 💖 Support

If you find MANA helpful, please consider:
- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting new features
- 📢 Sharing with others

---

## 📧 Contact

- **Issues:** [GitHub Issues](https://github.com/yourusername/mana/issues)
- **Email:** your.email@example.com
- **Twitter:** [@yourusername](https://twitter.com/yourusername)

---

<div align="center">

**Made with ❤️ by the MANA Team**

[⬆ Back to Top](#-mana)

</div>
