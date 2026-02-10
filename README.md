# MediaForge - Multi-Platform Media Downloader

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Platform: Windows](https://img.shields.io/badge/platform-Windows-lightgrey.svg)](https://www.microsoft.com/windows)

##  LEGAL NOTICE & DISCLAIMER

**THIS SOFTWARE IS PROVIDED FOR EDUCATIONAL AND RESEARCH PURPOSES ONLY.**

- You are **solely responsible** for ensuring you have the legal right to download any content
- Downloading copyrighted content without permission may violate platform Terms of Service and copyright laws
- This tool does NOT bypass DRM or access protection mechanisms
- Use of this software may violate Terms of Service of third-party platforms (YouTube, Instagram, TikTok, Facebook)
- The developer assume **NO LIABILITY** for misuse of this software
- Users must comply with all applicable local, national, and international laws

**By using this software, you acknowledge that you have read and understood this disclaimer.**


##  Features

-  **Multi-Platform Support**: YouTube, Instagram, TikTok, Facebook
-  **High-Quality Downloads**: Up to 4K resolution support (platform-dependent)
-  **Audio Extraction**: Convert videos to MP3 with customizable bitrate (up to 320kbps)
-  **Partial Downloads**: Download specific time ranges from videos
-  **Flexible Output**: Choose download location and file format


##  Quick Start

### Prerequisites

- **Python 3.8 or higher**
- **Windows OS** (Linux/Mac support coming soon)
- **Internet connection** for downloading media and FFmpeg

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Hmster004/mediaforge.git
   cd mediaforge
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Setup FFmpeg** (automatic)
   ```bash
   python scripts/setup_ffmpeg.py
   ```

4. **Run the application**
   ```bash
   python main.py
   ```

---

##  Usage Guide

### Basic Download

1. **Launch** the application by running `python main.py`, if you don't know how to this go to `dist/` and there is a .exe file.
2. **Paste** a valid media URL into the input field
3. **Wait** for automatic metadata and thumbnail loading
4. **Select** your preferred format (Video/Audio) and quality
5. **Choose** output folder (defaults to Downloads)
6. **Click** the Download button

### Advanced Features

#### Partial Download
- Enable "Partial Download" toggle
- Enter start time (format: `HH:MM:SS` or `MM:SS` or `SS`)
- Enter end time in the same format
- Download only the specified portion of the video

#### Quality Options

**Video:**
- Best Available 
- 4K / Ultra HD (2160p)
- 2K / QHD (1440p)
- 1080p (Full HD)
- 720p (HD)
- 480p (SD)
- 360p (Low)

**Audio:**
- 320kbps (Best)
- 256kbps (High)
- 192kbps (Standard)

---

##  Building Executable

To create a standalone `.exe` file:

```bash
pyinstaller MediaDownloader.spec
```

The executable will be in the `dist/` folder.

---

##  Project Structure

```
mediaforge/
├── core/                   # Core functionality
│   ├── config.py          # Configuration management
│   ├── downloader.py      # Main download orchestrator
│   ├── media_model.py     # Data models
│   ├── platform_base.py   # Abstract base for platforms
│   └── utils_logger.py    # Logging utilities
├── platforms/             # Platform-specific downloaders
│   ├── youtube.py
│   ├── instagram.py
│   ├── tiktok.py
│   └── facebook.py
├── gui/                   # User interface
│   ├── main_window.py
│   └── theme.py
├── scripts/               # Utility scripts
│   └── setup_ffmpeg.py
├── assets/                # Application resources
│   └── icon.ico
├── main.py               # Application entry point
├── requirements.txt      # Python dependencies
└── README.md            # This file
```

---

##  Configuration

Edit `core/config.py` to customize:

```python
class Config:
    APP_NAME = "MediaForge - By YourName"
    DEFAULT_DOWNLOAD_DIR = "path/to/your/downloads"
    COLORS = {...}  # You can costomize theme colors/name and sh
```

---

##  Running Tests

```bash
python -m pytest tests/
```

Or run the multi-platform test:

```bash
python test_multi_platform.py
```

---



### Development Setup

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/Feature`)
3. Commit your changes (`git commit -m 'Add some Feature'`)
4. Push to the branch (`git push origin feature/Feature`)
5. Open a Pull Request

---

##  Known Issues

- Partial Download only works for You Tube
- Quality of other platforms might be broken

See [Issues](https://github.com/yourusername/mediaforge/issues) for a complete list.

---


---

##  License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

##  Acknowledgments

- [yt-dlp](https://github.com/yt-dlp/yt-dlp) - Powerful video downloader library
- [PySide6](https://doc.qt.io/qtforpython-6/) - Qt for Python GUI framework
- [FFmpeg](https://ffmpeg.org/) - Multimedia processing framework

---

## 📧 Contact

**Developer**: Hamzter004  
**Project Link**: [https://github.com/yourusername/mediaforge](https://github.com/yourusername/mediaforge)
**Donations** :[https://buymeacoffee.com/hn59395sh] not required btw
---

##  Additional Legal Information

### Fair Use Consideration
This tool should only be used in accordance with fair use principles and applicable copyright laws. Fair use typically includes:
- Educational purposes
- Research and scholarship
- Personal archival of content you own or have permission to download
- Criticism, commentary, or parody (where applicable)

### Platform-Specific Policies
Be aware that downloading content may violate the Terms of Service of:
- **YouTube**: [Terms of Service](https://www.youtube.com/t/terms)
- **Instagram**: [Terms of Use](https://help.instagram.com/581066165581870)
- **TikTok**: [Terms of Service](https://www.tiktok.com/legal/terms-of-service)
- **Facebook**: [Terms of Service](https://www.facebook.com/terms.php)

### Creator Rights
Always respect content creators' rights. Consider:
- Supporting creators through official channels
- Respecting copyright notices and licensing
- Not redistributing downloaded content without permission
- Always support the creators.

---

** Give a star maybe **
