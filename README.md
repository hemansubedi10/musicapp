<div align="center">
  <img src="composeApp/icon/circle_app_icon.png" width="160" alt="HeMan Vibes Logo" />
  <h1>HeMan Vibes</h1>
  <p><strong>Next-Generation Cross-Platform Music Streaming Client</strong></p>
  <p>Crafted with Kotlin &amp; Compose Multiplatform for <b>Windows</b>, <b>macOS</b>, <b>Android</b>, and <b>Linux</b>.</p>

  <p>
    <a href="https://github.com/hemansubedi10/musicapp/releases/latest"><img src="https://img.shields.io/github/v/release/hemansubedi10/musicapp?style=for-the-badge&color=00d2ff&label=Latest%20Release" alt="Latest Release"></a>
    <a href="https://github.com/hemansubedi10/musicapp/stargazers"><img src="https://img.shields.io/github/stars/hemansubedi10/musicapp?style=for-the-badge&color=8b5cf6" alt="Stars"></a>
    <a href="https://github.com/hemansubedi10/musicapp/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-GPL%203.0-pink?style=for-the-badge" alt="License"></a>
  </p>
</div>

---

## 📥 Device-Wise Download Options

Download the ready-to-run installation package for your operating system:

| Platform / Device | Architecture | Package Format | Download Link |
| :--- | :--- | :--- | :--- |
| **🪟 Windows** | 64-bit (x64) / ARM64 | Installer ZIP / MSIX | [**Download for Windows (.zip)**](https://github.com/hemansubedi10/musicapp/releases/download/v1.0.0/HeManVibes-Windows-installer.zip) |
| **🍎 macOS** | Apple Silicon (M1 / M2 / M3 / M4) | Disk Image (.dmg) | [**Download for Mac Apple Silicon (.dmg)**](https://github.com/hemansubedi10/musicapp/releases/download/v1.0.0/HeManVibes-mac-aarch64.dmg) |
| **🍏 macOS** | Intel Core (x86_64) | Disk Image (.dmg) | [**Download for Mac Intel (.dmg)**](https://github.com/hemansubedi10/musicapp/releases/download/v1.0.0/HeManVibes-mac-amd64.dmg) |
| **🤖 Android** | Universal (All Devices + Auto) | APK Package (.apk) | [**Download for Android (.apk)**](https://github.com/hemansubedi10/musicapp/releases/download/v1.0.0/HeManVibes-Android-universal.apk) |
| **🐧 Linux** | 64-bit (x86_64) | Standalone AppImage | [**Releases Page**](https://github.com/hemansubedi10/musicapp/releases/latest) |

> **Windows Quick Setup**: Unzip `HeManVibes-Windows-installer.zip` and run `install.bat`, or use the portable silent launcher.  
> **Android Setup**: Download the `.apk` directly to your phone, tap to install, and allow installation from unknown sources.

---

## 🖼️ Application Interface & Screenshots

### Desktop Experience (Windows & macOS)
<p align="center">
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/19.png" width="95%" alt="HeMan Vibes Desktop Interface" style="border-radius: 12px; box-shadow: 0 8px 30px rgba(0,0,0,0.5);" />
</p>

### Mobile & Tablet Experience (Android)
<p align="center">
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/01.png" width="22%" alt="Now Playing Player" />
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/02.png" width="22%" alt="Apple Music Synced Lyrics" />
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/03.png" width="22%" alt="Synced Lyrics Romanization" />
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/04.png" width="22%" alt="Home Discover Feed" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/05.png" width="22%" alt="Moods and Genres" />
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/06.png" width="22%" alt="Top Charts" />
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/07.png" width="22%" alt="10-Band Equalizer" />
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/08.png" width="22%" alt="AutoEq Headphone Correction" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/09.png" width="22%" alt="Music Library" />
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/10.png" width="22%" alt="Offline Downloads" />
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/11.png" width="22%" alt="Artist Page" />
  <img src="https://raw.githubusercontent.com/hemansubedi10/musicapp/main/asset/screenshot/12.png" width="22%" alt="Shazam Song Identifier" />
</p>

---

## ✨ Core Features & Streaming Engine

- 🎧 **High-Quality Audio Playback**: Stream high-bitrate Opus and AAC audio directly using YouTube & YouTube Music algorithms with background playback and no ads.
- 🎶 **Apple Music-Style Synced Lyrics**: Real-time karaoke lyrics powered by LRCLIB, BetterLyrics, and YouTube transcript scrapers, with 12-language romanization and timing offset calibration.
- 🎚️ **Pro Audio Processing**: Built-in 10-band equalizer with AutoEq headphone correction curves, DJ-style crossfade, audio delay, and reverb effects.
- 🖥️ **Hardware-Accelerated Desktop**: Powered by `libmpv` C-runtime API for zero-lag audio rendering on Windows, macOS, and Linux.
- 📱 **Android Auto & Automotive**: Full automotive dashboard support and Home screen turntable & listening insight widgets.
- 📲 **QR Code Login Sync**: Securely sync your YouTube Music account and playlists from your Android device to your computer via a local network QR scan.
- 🔍 **Shazam Song Recognition**: Identify any track playing near you directly from the app or from the Android Quick Settings tile.
- 🛡️ **SponsorBlock & Return YouTube Dislike**: Automatically skips non-music intros, promotional segments, and sponsored interruptions.
- 📦 **Offline Caching & Smart Downloads**: Download tracks and albums for seamless offline listening anywhere.

---

## 🔒 Security & Privacy Notice

- **No Sensitive Credentials Stored**: All API secrets, private keystores, signing certificates, and local authentication tokens are strictly kept out of version control via `.gitignore` and Gradle BuildKonfig isolation.
- **Client-Side Direct Connection**: Streams communicate directly with official YouTube Music / Google Video servers with no tracking proxies or third-party intermediary servers.
- **Zero Telemetry in Open Builds**: Crash analytics are completely isolated and disabled for private user builds.

---

## 🏗️ Architecture & Modules

HeMan Vibes follows **Clean Architecture + MVVM** using JetBrains Compose Multiplatform:

```
┌────────────────────────────────────────────────────────┐
│               composeApp (Shared UI)                   │
│   - Jetpack Compose / Compose Multiplatform            │
│   - Shared ViewModels, Navigation, Material 3 Theme    │
├──────────────────────────┬─────────────────────────────┤
│   androidApp (Android)   │    desktopApp (JVM/Desktop) │
│   - ExoPlayer (Media3)   │    - libmpv C-runtime JNA   │
│   - Auto & Widgets       │    - CustomTitleBar, Tray   │
├──────────────────────────┴─────────────────────────────┤
│                      core/                             │
│   - domain: Domain Models, Use Cases, Interfaces       │
│   - data: Room DB, Offline Caches, Repositories        │
│   - service: YouTube Music Scraper, Lyrics, Spotify    │
│   - media: Media3 (Android) & media-jvm (Desktop)      │
└────────────────────────────────────────────────────────┘
```

---

## 🚀 Building & Running from Source

### Prerequisites
- **JDK 21** or newer (OpenJDK recommended)
- **Git**
- **Android SDK** (for Android builds)

### 1. Clone the Repository
```bash
git clone https://github.com/hemansubedi10/musicapp.git
cd musicapp
```

### 2. Fetch Desktop Native Binaries
Fetches pre-compiled `libmpv` native slices for Windows, macOS, and Linux:
```bash
./gradlew :composeApp:mpvSetupAll
```

### 3. Run Desktop Application (Windows, macOS, Linux)
```bash
./gradlew :desktopApp:run
```

### 4. Build Android Application
```bash
# Debug APK
./gradlew :androidApp:assembleDebug

# Release APK
./gradlew :androidApp:assembleRelease
```

---

## 👤 Author & Maintainer

**Heman Subedi**  
- GitHub: [@hemansubedi10](https://github.com/hemansubedi10)
- Project: [musicapp](https://github.com/hemansubedi10/musicapp)

---

## 📜 Acknowledgments

HeMan Vibes builds upon the open-source achievements of:
- [SimpMusic](https://github.com/maxrave-dev/SimpMusic) & [maxrave-dev](https://github.com/maxrave-dev) for the Compose Multiplatform foundation
- [InnerTune](https://github.com/z-huang/InnerTune) & [SmartTube](https://github.com/yuliskov/SmartTube) for YouTube Music API & streaming architecture
- [LRCLIB](https://lrclib.net/) & [BetterLyrics](https://github.com/BetterLyrics) for synchronized lyrics
- [SponsorBlock](https://sponsor.ajay.app/) for crowd-sourced sponsor skipping

---

## 📄 License
This project is licensed under the **GNU General Public License v3.0 (GPL-3.0)**.
