<div align="center">
  <img src="composeApp/icon/circle_app_icon.png" width="160" alt="HeMan Vibes Logo" />
  <h1>HeMan Vibes</h1>
  <p><strong>Next-Generation Cross-Platform Music Streaming Client</strong></p>
  <p>Crafted with Kotlin &amp; Compose Multiplatform for <b>Android</b>, <b>Windows</b>, <b>macOS</b>, and <b>Linux</b>.</p>

  <p>
    <a href="https://github.com/hemansubedi10/musicapp/releases"><img src="https://img.shields.io/github/v/release/hemansubedi10/musicapp?style=flat-square&color=00d2ff" alt="Latest Release"></a>
    <a href="https://github.com/hemansubedi10/musicapp/stargazers"><img src="https://img.shields.io/github/stars/hemansubedi10/musicapp?style=flat-square&color=8b5cf6" alt="Stars"></a>
    <a href="https://github.com/hemansubedi10/musicapp/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-GPL%203.0-pink?style=flat-square" alt="License"></a>
  </p>
</div>

---

## ✨ Highlights & Features

- 🎧 **Ad-Free Music Streaming**: High-speed, seamless streaming directly from YouTube & YouTube Music with full background playback support.
- 🎶 **Apple Music-Style Synced Lyrics**: Real-time, word-by-word synchronized karaoke lyrics with romanization for 12 languages and customizable timing offset.
- 🎨 **Modern Liquid Glass UI**: Built with Material Design 3 and custom desktop titlebars, sleek dark/light dynamic palettes, and animated album art.
- 🎚️ **Pro Audio Processing**: Built-in 10-band equalizer with AutoEq headphone correction profiles, DJ-style crossfade, delay, and studio reverb effects.
- 📱 **Android Auto & Home Widgets**: Turntable widgets, listening insights, and full automotive media dashboard integration.
- 🖥️ **Desktop Native Engine**: Powered by `libmpv` C-runtime for low-latency hardware audio playback on Windows, macOS, and Linux.
- 📲 **LAN QR Login Sync**: Securely sync your YouTube Music login and personal library from Android to your Desktop via a single QR code scan.
- 🔍 **Shazam Song Recognition**: Identify songs playing around you in seconds directly from the search bar or Android Quick Settings tile.
- 🛡️ **SponsorBlock & Return YouTube Dislike**: Automatically bypass non-music intros, sponsorships, and track skips.
- 📦 **Offline Caching**: Download tracks for offline playback with intelligent caching.

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

## 📦 Packaging Desktop Installers

Packaged using [Hydraulic Conveyor](https://conveyor.hydraulic.dev/):
- **Windows**: MSIX installer (`simpmusic-*.msix`)
- **macOS**: DMG disk images (`.dmg`) for Apple Silicon (`aarch64`) and Intel (`x64`)
- **Linux**: Standalone `.AppImage`

```bash
./gradlew :desktopApp:writeConveyorConfig
conveyor make site
```

---

## 👤 Author & Maintainer

**Heman Subedi**  
- GitHub: [@hemansubedi10](https://github.com/hemansubedi10)
- Project: [musicapp](https://github.com/hemansubedi10/musicapp)

---

## 📜 Acknowledgments & Open Source

HeMan Vibes stands on the shoulders of the open-source community:
- [SimpMusic](https://github.com/maxrave-dev/SimpMusic) & [maxrave-dev](https://github.com/maxrave-dev) for the original Compose Multiplatform foundation
- [InnerTune](https://github.com/z-huang/InnerTune) & [SmartTube](https://github.com/yuliskov/SmartTube) for YouTube Music API & streaming architecture
- [LRCLIB](https://lrclib.net/) & [BetterLyrics](https://github.com/BetterLyrics) for synchronized lyrics
- [SponsorBlock](https://sponsor.ajay.app/) for crowd-sourced sponsor skipping

---

## 📄 License
This project is licensed under the **GNU General Public License v3.0 (GPL-3.0)**.
