
<h1>Strata Notch</h1>

<p><strong>A modular, Liquid Glass Dynamic Island &amp; Notch Hub for macOS.</strong></p>

<p>
  <a href="https://github.com/ChenithaPalugaswewa/StrataNotch/raw/main/StrataNotch.zip">
    <img src="https://img.shields.io/badge/Download-StrataNotch.zip%20(2.4%20MB)-0A84FF?style=for-the-badge&logo=apple&logoColor=white" alt="Download StrataNotch.zip" />
  </a>
  <img src="https://img.shields.io/badge/macOS-15.0%2B%20Sequoia-000000?style=for-the-badge&logo=apple&logoColor=white" alt="macOS 15.0+" />
  <img src="https://img.shields.io/badge/macOS%2026-Liquid%20Glass-5856D6?style=for-the-badge&logo=apple&logoColor=white" alt="macOS 26 Liquid Glass" />
  <img src="https://img.shields.io/badge/Arch-Apple%20Silicon%20%26%20Intel-34C759?style=for-the-badge" alt="Universal Binary" />
  <img src="https://img.shields.io/badge/License-MIT-F59E0B?style=for-the-badge" alt="MIT License" />
</p>

<p>
  <a href="#download--install">Download</a> •
  <a href="#overview">Overview</a> •
  <a href="#island-states">Island States</a> •
  <a href="#expanded-hub-features">Expanded Hub</a> •
  <a href="#gestures--shortcuts">Gestures &amp; Shortcuts</a> •
  <a href="#customization--themes">Customization</a> •
  <a href="#permissions--privacy">Permissions</a> •
  <a href="https://chenithapalugaswewa.github.io/StrataNotch/">Website</a>
</p>

</div>


<img width="688" height="324" alt="Screenshot 2026-11-18 at 5 24 06 pm" src="https://github.com/user-attachments/assets/ce5d6c6e-5b34-40d3-ab86-7d53ecf11358" />
<div align="center">

---

## Download & Install

> **[Download `StrataNotch.zip` (v1.0 • Universal Binary • 2.4 MB)](https://github.com/ChenithaPalugaswewa/StrataNotch/raw/main/StrataNotch.zip)**

1. Download and unzip **`StrataNotch.zip`**.
2. Drag **`Strata Notch.app`** into your **`/Applications`** folder.
3. Launch **Strata Notch** from `/Applications`.
   - *Note (ad-hoc signed build):* If macOS Gatekeeper blocks the first launch, run `xattr -cr "/Applications/Strata Notch.app"` in Terminal or click **Open Anyway** in **System Settings → Privacy & Security**.

---

## Overview

**Strata Notch** transforms the MacBook hardware notch — or an adaptive, pill-shaped Dynamic Island on notchless Macs and external monitors — into a fast, click-through, non-activating control hub and live HUD.

Built natively in Swift with **AppKit (`NSPanel`)** and **SwiftUI (`@Observable`)**, Strata Notch stays quietly integrated into your top bezel until you hover, pull down, drag a file, or trigger a system event. On **macOS 26 (Tahoe)** it renders with native **Liquid Glass** (`glassEffect` & `GlassEffectContainer`), with an automatic `.ultraThinMaterial` fallback on **macOS 15 (Sequoia)**.

---

## Island States

Strata Notch fluidly morphs across four states powered by spring physics:

| State | Behavior |
| :--- | :--- |
| **Dormant Bezel** | Click-through overlay aligned to the notch or bezel. Supports **7 ambient modes**: *Hidden*, *Live Clock*, *Battery Dot*, *Weather*, *Clock + Battery*, *Clock + Weather*, and *System Pulse* (CPU/RAM), plus a *Keep Awake* indicator badge. |
| **Compact Live Activity** | Expands symmetric wings beside the notch whenever media is playing or a timer/Pomodoro/stopwatch is running. Configurable across **3 density styles**: *Minimal Dots*, *Standard*, and *Rich Info*. |
| **Detached HUD Alerts** | Coalescing floating pill beneath the bezel for hardware & system events: Volume, Mute, Brightness, Charger Plug/Wattage, Low Battery (`<20%`), Full Charge (`100%`), Wi-Fi/Ethernet status, Bluetooth connect/disconnect, Track Change banners, Focus toggles, File Shelf/AirDrop feedback, Active Downloads progress, Area Screenshots, and Notification mirroring. |
| **Expanded Hub** | Full interactive workspace with a symmetric header bar, a drag-reorderable **Crystal-Clear Liquid Dock** tab bar, and a continuous horizontal swipe carousel across **6 tabs**: *Home*, *Media*, *Shelf*, *Focus*, *Weather*, and *System*. |

### Native OS HUD Replacement
Enable **Suppress Native OS Volume/Brightness HUD** (requires Accessibility permission) to intercept system media keys (`Volume Up/Down`, `Mute`, `Brightness Up/Down`) via `CGEventTap` — replacing macOS's centered OSD with Strata Notch's compact HUD, complete with fine-grained `⌥ + ⇧` (1/64 step) adjustments.

---

## Expanded Hub Features

### 1. Home
- **Time-Aware Greeting & Live Clock**: Dynamic greeting (*Good Morning / Afternoon / Evening*) with live time and date.
- **Now Playing Glance**: Mini artwork, title/artist, play/pause & skip controls — automatically falls back to a **System CPU & Battery** glance card when no media is active.
- **Weather Glance**: Current temperature, condition icon, High/Low, humidity %, and GPS/city status badge.
- **Quick Sliders**: Direct **Output Volume** (with mute button) and **Display Brightness** sliders.
- **Calendar Glance**: Shows your next non-all-day event within the next 24 hours via **EventKit**, with calendar color coding and automatic **Join Meeting** link detection for **Zoom, Google Meet, Microsoft Teams, Webex, FaceTime, Around, Whereby, Gather, and Discord**.

### 2. Media & Audio
- **Multi-Source Now Playing**:
  - **Apple Music** & **Spotify** via Distributed Notifications and AppleScript (`title`, `artist`, `album`, `artwork`, `duration`, `elapsed position`, interactive timeline scrubbing, and transport controls).
  - **11 Supported Web Browsers**: *Safari*, *Safari Technology Preview*, *Orion*, *Google Chrome*, *Chrome Canary*, *Arc*, *Brave*, *Microsoft Edge*, *Vivaldi*, *Opera*, and *Dia* — intelligently prioritizing active audio playback and the frontmost browser.
  - **One-Click Source Activation**: Click the album artwork or app button to jump straight to the playing app; includes an inline prompt if macOS Automation permission is denied.
- **Live 6-Bar FFT Equalizer**: Real-time system audio spectrum analyzer powered by **ScreenCaptureKit** + **Accelerate (`vDSP` 1024-sample Hann-windowed FFT)** when Screen & Audio Recording is granted, with a smooth simulated motion fallback when disabled.
- **Bluetooth Device Battery Badge**: Live battery readout for connected Bluetooth audio gear via **IOKit** & `system_profiler`, including split **Left / Right / Case %** support for AirPods and compatible earbuds.
- **10-Band Real-Time Bluetooth Equalizer**:
  - Uses **CoreAudio Process Tap** (`AudioHardwareCreateProcessTap` + Aggregate Device) when a Bluetooth audio device is the active output.
  - **10 Bands (`±12 dB`)**: `32`, `64`, `125`, `250`, `500`, `1K`, `2K`, `4K`, `8K`, `16K Hz`.
  - **5 Presets**: *Flat*, *Bass Boost*, *Vocal*, *Spatial*, and *Custom*, plus an instant **Bypass** toggle.

### 3. File Shelf & Downloads
- **Drag-from-Anywhere Auto-Open**: Dragging any file near the top bezel automatically reveals the Shelf & AirDrop drop targets.
- **Persistent File Shelf**:
  - Asynchronous **QuickLook** thumbnails, file size formatting, **Open**, **Reveal in Finder**, single-item **AirDrop**, remove, and drag-out support to any app.
  - Add files via drag-and-drop or the `+ Add` Finder picker.
- **Dedicated AirDrop Drop Zone**: Drop files directly onto the AirDrop tile (or click to pick files) to invoke `NSSharingService` immediately.
- **Live Downloads Watcher**:
  - Monitors `~/Downloads` in real time using `DispatchSource` + `Foundation.Progress` subscribers.
  - Tracks in-progress browser downloads (`.download`, `.crdownload`, `.part`, `.partial`, `.incomplete`, `.opdownload`, `.tmp`) with live HUD progress bars and completion rings, alongside a recent Downloads grid with click-to-open and drag-out.

### 4. Focus & Productivity
- **Timer, Pomodoro & Stopwatch**:
  - **Timer**: Quick `1m`, `5m`, `10m`, `15m`, `30m` presets and `+1m` live adjustment.
  - **Pomodoro**: `Focus Session` (25m), `Short Break` (5m), and `Long Break` (15m) phases with completed session tracking.
  - **Stopwatch**: High-precision tenths-of-a-second readout.
  - Sleep-proof date-based countdowns with compact bezel wings and completion pulse alerts.
- **Live Camera Mirror**:
  - Instant horizontally mirrored front/FaceTime camera preview (`AVCaptureSession` + `AVCaptureVideoPreviewLayer`).
  - Completely stops the session and removes hardware inputs on close so the Mac's green camera LED turns off immediately.
- **Clipboard History, Notes Scratchpad & Shortcuts**:
  - **Clipboard History**: Tracks up to **10** recent text snippets and SHA-256-deduplicated, downsampled images; automatically ignores password managers and concealed pasteboard types (`org.nspasteboard.ConcealedType`, `TransientType`, `AutoGeneratedType`, `com.agilebits.onepassword`).
  - **Scratchpad**: Persistent monospace quick-notes editor right inside the notch (temporarily promotes the panel to key window only while editing).
  - **Shortcuts Runner**: Lists and executes your macOS **Shortcuts** (`/usr/bin/shortcuts`) directly from the hub.
- **Focus Mode Bar**: Displays and toggles macOS Focus modes (*Do Not Disturb*, *Work*, *Personal*, *Sleep*, or custom modes) via zero-flicker Shortcuts CLI or Control Center Accessibility fallback — includes a **1-click silent Focus shortcut installer**.

### 5. Weather
- **Zero-API-Key Weather Pipeline**: Powered by **Open-Meteo** (forecast + city geocoding) with **CoreLocation GPS**, automatic **GeoJS IP** fallback, and optional **Custom City** override in Settings.
- **Forecast Details**: `°C` / `°F` toggle, *Feels Like*, daily *High / Low*, *Wind Speed* (`km/h`), *Humidity %*, and a **4-hour hourly forecast** with precipitation probability.

### 6. System & Quick Utilities
- **2×2 Live Telemetry Grid** (sampled every 2s while active):
  - **CPU**: Multi-core average load % via `host_processor_info` with a 24-point smooth sparkline.
  - **Memory**: Ring gauge + GB breakdown (*Active*, *Wired*, *Compressed*, *Total*).
  - **Network**: Dual-curve Download (`↓`) / Upload (`↑`) throughput sparkline + clickable toggle to inspect **Wi-Fi SSID & Signal RSSI (`dBm`)** via **CoreWLAN**.
  - **Power & Storage**: Battery %, AC/Charging state, SmartBattery **charger wattage (`W`)**, time remaining, connected Bluetooth audio battery badge, and **SSD free space**.
- **Quick Utilities Strip**:
  - **Keep Awake** (`IOPMAssertion` display caffeinate)
  - **Mute Audio** (CoreAudio output mute toggle)
  - **Bluetooth EQ** (inline preset & bypass menu + shortcut to full 10-band EQ)
  - **Focus Toggle**
  - **Area Screenshot** (collapses the island and launches interactive `screencapture -ic` straight to your clipboard with a HUD confirmation)

---

## Gestures & Shortcuts

### Trackpad & Mouse Gestures
| Action | Result |
| :--- | :--- |
| **Hover over Dormant / Compact Bezel** | Opens Expanded Hub (configurable hover delay `0.15s – 0.80s`) |
| **Pull Down from Top Bezel** | Siri-style drag gesture to open Expanded Hub |
| **Pull Up on Notch Cap** | Drag gesture to collapse Expanded Hub |
| **Click Dormant / Compact Island** | Expands into the Hub |
| **Two-Finger Horizontal Swipe** | Switches tabs smoothly inside the Expanded Hub |
| **Drag File Near Top Bezel** | Auto-opens the Shelf & AirDrop drop zones |
| **Pin Open Button** | Locks the Expanded Hub open until unpinned or collapsed |
| **Outside Click / Fullscreen App** | Collapses automatically (auto-hides during fullscreen video/apps if enabled) |

### Menu Bar Keyboard Shortcuts
| Shortcut | Action |
| :--- | :--- |
| `⌘ I` | Show / Hide Notch Island |
| `⌘ E` | Expand / Collapse Hub |
| `⌘ M` | Toggle Live Camera Mirror |
| `⌘ T` | Trigger Sample HUD Alert |
| `⌘ ,` | Open Settings |
| `⌘ Q` | Quit Strata Notch |

---

## Customization & Themes

Open **Settings (`⌘,`)** or click the gear icon in the Expanded Hub header:

- **4 Visual Themes**:
  - **Liquid Glass** — Native macOS 26 `glassEffect` (with macOS 15 translucent glass fallback)
  - **Pure Black** — Seamless OLED-style bezel blend
  - **Midnight Graphite** — Deep smoked slate with cool steel accents
  - **Arctic Frost** — Bright frosted aluminum tint
- **3 Bezel Shapes**: *Classic Notch*, *Soft Pill*, *Minimal Drop* (plus an option to use the floating Pill style even on Macs with a physical notch).
- **3 Rim Glow Styles**: *None*, *Subtle Frost*, *Adaptive Activity* (tints rim glow to active media artwork, timers, or Focus mode).
- **Geometry & Behavior**: Adjust width & height offsets, corner radius, background opacity, hover-to-open delay, fullscreen auto-hide, **Launch at Login** (`SMAppService`), and **drag-to-reorder Dock tabs**.
- **10 Core Modules & 11 Modular Extensions**: Independently toggle every feature (Media, Hardware HUD, OS HUD Suppressor, File Shelf, Timers, Clipboard & Scratchpad, Camera Mirror, Weather, Calendar, System Telemetry, plus Downloads Watcher, AirDrop Zone, Bluetooth Battery, 10-Band EQ, Shortcuts Runner, Focus Sync, Disk Telemetry, Track Banners, Connectivity Alerts, Notification Mirroring, and Audio Waveform).
- **Backup & Restore**: **Export**, **Import**, or **Reset** all preferences as JSON.

---

## Permissions & Privacy

Strata Notch processes everything **locally on your Mac** with **no analytics, no telemetry, and no external accounts**. Permissions are only requested when you use or enable the corresponding module:

| Permission | Used For |
| :--- | :--- |
| **Accessibility** | Suppressing the native macOS Volume/Brightness OSD, Control Center Focus fallback, and Notification Center HUD mirroring |
| **Automation (Apple Events)** | Reading playback metadata and sending transport/scrub commands to Apple Music, Spotify, and supported browsers |
| **Screen & System Audio Recording** | Capturing system audio buffers via ScreenCaptureKit for the real-time 6-band FFT equalizer (no screen pixels are stored or recorded) |
| **Camera** | Live Camera Mirror preview (immediately stops hardware capture on close) |
| **Calendars** | Displaying your next upcoming event and meeting link in Calendar Glance |
| **Location Services** | Local GPS coordinates for Weather (falls back automatically to IP geolocation or custom city) |
| **Downloads Folder** | Monitoring `~/Downloads` for active download progress and recent items |

A built-in **Permissions & Diagnostics** checklist in Settings lets you verify status at a glance, jump straight to the right System Settings pane, and detect duplicate app bundles in `/Applications` that can confuse macOS TCC permissions.

---

## Requirements & Compatibility

- **macOS 15.0 (Sequoia)** or later *(macOS 26.0 Tahoe enables native Liquid Glass APIs)*
- **Apple Silicon (`arm64`)** & **Intel (`x86_64`)** Universal binary
- Works on MacBooks with a physical notch as well as notchless Macs and external monitors (Dynamic Island Pill mode)

---

<div align="center">
  <p>Crafted by <strong>Chenitha Palugaswewa • Strata</strong></p>
  <p><sub>MIT License • © 2026 Chenitha Palugaswewa</sub></p>
</div>
