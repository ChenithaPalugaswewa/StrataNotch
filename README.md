<div align="center">

<h1>Strata Notch</h1>

<p><strong>A modular, Liquid Glass Dynamic Island &amp; Notch Control Center for macOS.</strong></p>

<p>
  <a href="https://stratanotch.onrender.com">
    <img src="https://img.shields.io/badge/Website-stratanotch.onrender.com-7C3AED?style=for-the-badge&logo=safari&logoColor=white" alt="Live Website" />
  </a>
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
  <a href="#whats-new">What's New</a> •
  <a href="#island-states">Island States</a> •
  <a href="#expanded-hub-features">Expanded Hub</a> •
  <a href="#gestures--shortcuts">Gestures &amp; Shortcuts</a> •
  <a href="#customization--themes">Customization</a> •
  <a href="#permissions--privacy">Permissions</a> •
  <a href="https://stratanotch.onrender.com">Website</a>
</p>

</div>

---

<img width="732" height="344" alt="Screenshot 2026-11-18 at 5 45 44 pm" src="https://github.com/user-attachments/assets/37acd848-b8e4-4f1b-9b4f-660d3c92f6ab" />




## Download & Install

> **Official Website:** **[https://stratanotch.onrender.com](https://stratanotch.onrender.com)**  
> **Direct Download:** **[Download `StrataNotch.zip` (v1.0 • Universal Binary • 2.4 MB)](https://github.com/ChenithaPalugaswewa/StrataNotch/raw/main/StrataNotch.zip)**

1. Download and unzip **`StrataNotch.zip`**.
2. Drag **`Strata Notch.app`** into your **`/Applications`** folder.
3. Launch **Strata Notch** from `/Applications`.
   - *Note (ad-hoc signed build):* If macOS Gatekeeper blocks the first launch, run `xattr -cr "/Applications/Strata Notch.app"` in Terminal or click **Open Anyway** in **System Settings → Privacy & Security**.

---

## Overview

**Strata Notch** transforms the MacBook hardware notch — or an adaptive, floating **Dynamic Island Pill** with a simulated TrueDepth optics cluster on notchless Macs and external monitors — into a fast, click-through, non-activating control hub and live HUD.

Built natively in Swift with **AppKit (`NSPanel`)** and **SwiftUI (`@Observable`)**, Strata Notch stays quietly integrated into your top bezel until you hover, pull down like Siri, click, drag a file, or trigger a system event. On **macOS 26 (Tahoe)** it renders with native **Liquid Glass** (`glassEffect` & `GlassEffectContainer`), with an automatic `.ultraThinMaterial` glass fallback on **macOS 15 (Sequoia)**.

---


## What's New in the Latest Update


## Introducing Sidekick (Vertical Edge Dock)

<img width="934" height="556" alt="Screenshot 2026-11-19 at 5 05 11 pm" src="https://github.com/user-attachments/assets/671a45a3-d783-4898-93f2-b49ed629ccc2" />
<img width="393" height="433" alt="Screenshot 2026-11-19 at 5 05 29 pm" src="https://github.com/user-attachments/assets/4eee4a6d-007f-4f16-ba42-11d516b6aa03" />

<img width="302" height="156" alt="Screenshot 2026-11-19 at 5 07 41 pm" src="https://github.com/user-attachments/assets/17de3013-5ae8-4414-9288-5e8ff352c51e" />

**Sidekick** is a new **vertical screen-edge placement mode** in Strata Notch that lets you anchor the hub to the **Left** or **Right** edge of your display instead of (or whenever you switch from) the top hardware notch.

Switch anytime in **Settings (`⌘,`) → Screen Placement → Sidekick**, with a smooth animated transition between **Top Notch**, **Sidekick (Left)**, and **Sidekick (Right)**.

---

### How Sidekick Works

| State | Behavior |
| :--- | :--- |
| **Auto-Tucked Edge Badge** | Rests as a compact `44 × 44 pt` badge anchored to your chosen screen edge. When **Auto-Tuck Into Screen Edge When Idle** is enabled *(default)*, ~48% tucks unobtrusively into the bezel and slides out flush the instant your cursor approaches. |
| **Live Compact Icon** | Displays the Strata vector emblem when idle, or morphs directly into your **Now Playing album artwork**, live **Timer / Pomodoro countdown**, or **Charging / Battery** glyph when a Live Activity is running. |
| **Hover Info Pill & Side HUD Popups** | Hovering over the Sidekick icon reveals a floating Liquid Glass capsule pill beside it showing live **Now Playing + equalizer bars**, **active Timer**, **Time & Weather**, **Battery %**, and **Keep Awake** status. System HUD alerts (Volume, Brightness, Track Change, Downloads, Notifications) also pop right out beside the icon. |
| **Morphing Vertical Hub** | Stretches fluidly out of the `44 × 44` edge icon into a `418 × 434 pt` vertical control center featuring a **vertical Crystal-Clear Liquid Dock rail** along the screen edge and vertical-stack layouts tailored for **Home**, **Media**, **Shelf**, **Focus**, **Weather**, and **System**. |

---

### Sidekick Gestures & Controls

| Action | Result |
| :--- | :--- |
| **Hover over Sidekick Icon** | Shows the **Compact Info Pill** *(when Click to Open is enabled)* or **Auto-Expands** the full Sidekick hub *(when Click to Open is off, configurable `0.05s – 0.75s` delay)*. |
| **Click or Pull Outward from Screen Edge** | Smoothly stretches and morphs open the Sidekick hub (`≥ 14 pt` outward drag or flick). |
| **Drag Inward on the Outer Edge Bezel** | Squeezes and collapses the Sidekick hub back into the screen edge (`≥ 20 pt` inward drag on the outer `22 pt` bezel). |
| **Two-Finger Trackpad Scroll (Expanded)** | Cycles up/down through the 6 vertical tabs (automatically yields when scrolling inside overflowing lists like Clipboard, Shortcuts, or File Shelf). |
| **Two-Finger Trackpad Scroll (Compact Hover)** | Switches between active **Media ↔ Timer** Live Activities when both are running, or skips **Next / Previous** tracks. |
| **Drag Files to the Screen Edge** | Auto-expands Sidekick directly to the **File Shelf & AirDrop** drop zones. |

---

### Sidekick Customization (Settings → Sidekick)

When **Sidekick** is selected under **Screen Placement**, Settings automatically reveals dedicated Sidekick controls:

- **Screen Edge**: Anchor Sidekick to the **Left** or **Right** edge of your display.
- **Click to Open (Hover Shows Info Pill)**: Choose between a hover **Info Pill** (click or pull outward to expand) or automatic **Hover-to-Expand** (`0.05s – 0.75s` delay).
- **Auto-Tuck Into Screen Edge When Idle**: Tuck the idle badge half-way into the bezel until hovered.
- **Vertical Screen Position (`15% – 85%`)**: Slide Sidekick higher or lower along the left/right screen edge.
- **Sidekick Style & Size**: Customize **Rim Glow** (*None*, *Subtle Frost*, *Adaptive Activity*), **Icon Corner Radius (`-4…+8 pt`)**, **Icon Opacity (`80%–100%`)**, **Expanded Panel Width (`-40…+80 pt`)**, and **Expanded Panel Height (`-8…+24 pt`)**.


- **Configurable Open Trigger Modes**: Choose between **Hover or Drag Down** *(default)*, **Hover to Open**, or **Drag Down (Like Siri)** with 1:1 rubber-band physics, velocity-aware release, and zero-snap spring morphing.
- **Snappier Hover & Bezel Geometry**: Tuned default hover expansion delay to **`0.09s`** (`0.05s – 0.75s` range) with refined width (`+22 pt`) and height (`+1 pt`) default offsets and zero horizontal bleed over adjacent menu bar icons.
- **Integrated Top-Bar HUD Wings**: Hardware & system alerts (Volume, Brightness, Charger, Connectivity, Downloads, Notifications, Focus) now expand seamlessly as **symmetric top-bar wings** flanking the notch or Dynamic Island pill instead of a detached popup bubble.
- **Dynamic Island Pill Optics & Smart Auto-Reservation**: Automatically reserves the floating **Dynamic Island Pill** (`10 pt` top detachment gap + realistic camera/sensor optics cluster) on notchless Macs and external monitors, with a one-click toggle to use the Dynamic Island Pill on notched MacBooks too.
- **Full Web Media DOM Control & Tab Focus**: Direct JavaScript DOM playback control (`Play/Pause`, `Next/Previous` button click or `±15s` skip, and interactive **timeline scrubbing/seeking**) across 11 browsers, **YouTube oEmbed** author & HD thumbnail fetching, notification count badge stripping (`(3) ...`), and **one-click browser tab activation** that focuses the exact playing window and tab.
- **Granular Wi-Fi & Download Tracker Extensions**: Added dedicated toggles for **CoreWLAN Wi-Fi SSID, Signal & Power Toggle** and the **Download Tracker Pop-Out Pill** (with animated indeterminate & determinate progress bars).
- **Non-Nagging Permission Helper & Sandbox Migration**: Prompts macOS Accessibility and Screen Capture modals at most once, detects competing `/Applications` copies with a **Reveal App** shortcut, and automatically migrates legacy sandboxed preferences on launch.
- **15-Module Quick Toggle Menu**: Toggle 15 core modules and extensions directly from the macOS menu bar icon under **Active Modules**.



---

## Island States

Strata Notch fluidly morphs across four states powered by tuned spring physics:

<img width="512" height="64" alt="Screenshot 2026-11-18 at 5 44 58 pm" src="https://github.com/user-attachments/assets/50cd88dc-5bd6-4098-a2c7-cb7381539bff" />

<img width="466" height="76" alt="Screenshot 2026-11-18 at 5 44 51 pm" src="https://github.com/user-attachments/assets/565fceba-3d57-46d1-a1f3-7d1816a841a6" />


| State | Behavior |
| :--- | :--- |
| **Dormant Bezel** | Click-through pure-black hardware cap or floating Dynamic Island pill. Supports **7 ambient modes**: *Pure Black (Hidden)*, *Battery Dot*, *Live Clock*, *Live Weather*, *Clock + Battery*, *Clock + Weather*, and *System Pulse (CPU & RAM)*, plus an automatic *Keep Awake* indicator badge. |
| **Compact Live Activity** | Expands symmetric wings beside the notch whenever media is playing or a timer/Pomodoro/stopwatch is running. Configurable across **3 wing density styles**: *Minimal Dots*, *Standard (Artwork + Bars)*, and *Rich (Track & Details)*. |
| **Integrated Top-Bar HUD** | Coalescing top-bar wing expansion for hardware & system events: Volume, Mute, Brightness, Charger Plug/Wattage, Low Battery (`<20%`), Full Charge (`100%`), Wi-Fi/Ethernet status, Bluetooth connect/disconnect, optional Track Change banners, Focus toggles, File Shelf/AirDrop feedback, Live Download progress, Area Screenshots, and Notification mirroring. |
| **Expanded Hub** | Full interactive Liquid Glass drawer emerging smoothly from the physical notch with a symmetric header bar, a drag-reorderable **Crystal-Clear Liquid Dock** tab bar, and a continuous horizontal swipe carousel across **6 tabs**: *Home*, *Media*, *Shelf*, *Focus*, *Weather*, and *System*. |

### Native OS HUD Replacement
Enable **Suppress macOS Native Volume & Brightness HUD** (requires Accessibility permission) to intercept system media keys (`Volume Up/Down`, `Mute`, `Brightness Up/Down`) via `CGEventTap` — replacing macOS's centered OSD overlay with Strata Notch's integrated top-bar HUD, complete with fine-grained `⌥ + ⇧` (1/64 step) adjustments.

---

## Expanded Hub Features

### 1. Home
- **Time-Aware Greeting & Live Clock**: Dynamic greeting (*Good Morning / Afternoon / Evening*) with live time and date.
- **Now Playing Glance**: Mini artwork, title/artist, play/pause & skip controls — automatically falls back to a **System CPU & Battery** glance card when no media is active.
- **Weather Glance**: Current temperature, condition icon, High/Low, humidity %, and GPS/city status badge.
- **Quick Sliders**: Direct **Output Volume** (with mute button) and **Display Brightness** sliders.
- **Calendar "Up Next" Glance**: Shows your next non-all-day event within the next 24 hours via **EventKit**, with calendar color coding and automatic **1-click Join Meeting** link detection for **Zoom, Google Meet, Microsoft Teams, Webex, FaceTime, Around, Whereby, Gather, and Discord**.

### 2. Media & Audio

<img width="1447" height="877" alt="Screenshot 2026-11-18 at 6 12 48 pm" src="https://github.com/user-attachments/assets/39f8c2be-4ea0-4a9c-91b2-a0f08258b1e0" />

- **Universal Multi-Source Now Playing**:
  - **Apple Music** & **Spotify** via instant Distributed Notifications (`com.apple.Music.playerInfo`, `com.spotify.client.PlaybackStateChanged`), CoreAudio output-running listeners, and AppleScript (`title`, `artist`, `album`, `artwork`, `duration`, `elapsed position`, interactive timeline scrubbing, and transport controls).
  - **11 Supported Web Browsers**: *Safari*, *Safari Technology Preview*, *Orion*, *Google Chrome*, *Chrome Canary*, *Arc*, *Brave*, *Microsoft Edge*, *Vivaldi*, *Opera*, and *Dia* — inspecting HTML5 `<video>` / `<audio>` DOM state, MediaSession metadata, and **YouTube oEmbed** thumbnails (`youtube.com`, `youtu.be`, `shorts`, `live`).
  - **Full Browser Transport & Tab Focus**: Play/Pause, Next/Previous track (or `±15s` seek), interactive timeline scrubbing in web players, and **one-click source activation** that brings the exact playing browser tab to the front.
- **Live 6-Bar FFT Equalizer**: Real-time system audio spectrum analyzer powered by **ScreenCaptureKit** + **Accelerate (`vDSP` 1024-sample Hann-windowed FFT)** when Screen & System Audio Recording is granted, with a smooth simulated motion fallback when disabled.
- **Bluetooth Device Battery Breakdown**: Live battery readout for connected Bluetooth audio gear via **IORegistry** & `system_profiler`, including split **Left / Right / Case %** badges for AirPods and compatible earbuds.
- **Universal 10-Band Bluetooth Equalizer**:
  - Uses **CoreAudio Process Tap** (`AudioHardwareCreateProcessTap` + Aggregate Device) when a Bluetooth audio device is the active output.
  - **10 Bands (`±12 dB`)**: `32`, `64`, `125`, `250`, `500`, `1K`, `2K`, `4K`, `8K`, `16K Hz`.
  - **5 Presets**: *Flat*, *Bass Boost*, *Vocal*, *Spatial*, and *Custom*, plus an instant **Bypass** toggle.

### 3. File Shelf & Downloads


<img width="1457" height="876" alt="Screenshot 2026-11-18 at 6 13 07 pm" src="https://github.com/user-attachments/assets/a615f7d0-e60e-4650-94e3-1545b4727f41" />

- **Drag-from-Anywhere Auto-Open**: Dragging any file near the top bezel automatically expands the Shelf & AirDrop drop targets and holds the shelf open briefly after drop.
- **Persistent File Shelf**:
  - Asynchronous **QuickLook** thumbnails, file size formatting, **Open**, **Reveal in Finder**, single-item **AirDrop**, remove, and drag-out support to any app.
  - Add files via drag-and-drop or the `+ Add` Finder picker.
- **Dedicated AirDrop Drop Zone**: Drop files directly onto the right-hand AirDrop zone (or click to pick files) to invoke `NSSharingService(.sendViaAirDrop)` immediately.
- **Downloads Folder Watcher & Pop-Out Tracker Pill**:
  - Monitors `~/Downloads` in real time using `DispatchSource` + `Foundation.Progress` subscribers.
  - Tracks in-progress browser downloads (`.download`, `.crdownload`, `.part`, `.partial`, `.incomplete`, `.opdownload`, `.tmp`) with a live **Download Tracker Pop-Out Pill** (determinate progress bar or animated indeterminate bar), alongside a recent Downloads switcher inside the File Shelf tab.

### 4. Focus & Productivity

<img width="1470" height="873" alt="Screenshot 2026-11-18 at 6 13 16 pm" src="https://github.com/user-attachments/assets/c9bfaca9-71fa-438f-9597-5bc4bd3bc942" />

- **Timers, Pomodoro & Stopwatch**:
  - **Timer**: Quick `1m`, `5m`, `10m`, `15m`, `30m` presets and `+1m` live adjustment (expanding a live compact timer jumps straight to the Focus tab).
  - **Pomodoro**: `Focus Session` (25m), `Short Break` (5m), and `Long Break` (15m) phases with completed session tracking.
  - **Stopwatch**: High-precision tenths-of-a-second readout.
  - Sleep-proof date-based countdowns with compact bezel wings and completion pulse alerts.
- **Quick Camera Mirror**:
  - Instant horizontally mirrored front/FaceTime camera preview (`AVCaptureSession` + `AVCaptureVideoPreviewLayer`).
  - Immediately tears down the capture session when the island collapses or switches tabs so the Mac's green camera LED turns off right away.
- **Clipboard History, Notes Scratchpad & Shortcuts**:
  - **Clipboard History**: Tracks up to **10** recent text snippets and SHA-256-deduplicated, downsampled images; automatically ignores password managers and concealed pasteboard types (`org.nspasteboard.ConcealedType`, `TransientType`, `AutoGeneratedType`, `com.agilebits.onepassword`).
  - **Scratchpad**: Persistent monospace quick-notes editor inside the notch (temporarily promotes the panel to key window only while typing, then restores focus to your previous app).
  - **macOS Shortcuts Runner**: Lists and executes your macOS **Shortcuts** (`/usr/bin/shortcuts`) directly from the Focus tab.
- **Focus / Do Not Disturb Toggles**: Displays live Focus mode status in the header and toggles macOS Focus modes (*Do Not Disturb*, *Work*, *Personal*, *Sleep*, or custom modes) via zero-flicker Shortcuts CLI or Control Center Accessibility fallback — includes a **1-click silent Focus shortcut installer**.

### 5. Weather

<img width="1469" height="875" alt="Screenshot 2026-11-18 at 6 13 24 pm" src="https://github.com/user-attachments/assets/793f9935-6e79-4754-8aaa-b021ec5abd8c" />

- **Zero-API-Key Weather Pipeline**: Powered by **Open-Meteo** (forecast + city geocoding) with **CoreLocation GPS**, automatic **GeoJS IP** fallback, and optional **Custom City** override in Settings.
- **Forecast Details**: `°C` / `°F` toggle, *Feels Like*, daily *High / Low*, *Wind Speed* (`km/h`), *Humidity %*, and a **4-hour hourly forecast** with precipitation probability.

### 6. System & Quick Utilities

![Uploading Screenshot 2026-11-18 at 6.13.33 pm.png…]()

- **2×2 Live Telemetry Grid** (sampled every 2s while active, zero-polling IOKit power notifications):
  - **CPU**: Multi-core average load % via Mach `host_processor_info` with a 24-point smooth sparkline.
  - **Memory**: Ring gauge + GB breakdown (*Active*, *Wired*, *Compressed*, *Total*).
  - **Network & Wi-Fi**: Dual-curve Download (`↓`) / Upload (`↑`) throughput sparkline + **CoreWLAN Wi-Fi SSID, RSSI (`dBm`) signal readout, and one-click Wi-Fi power toggle**.
  - **Power & Storage**: Battery %, AC/Charging state, SmartBattery **charger wattage (`W`)**, time remaining, connected Bluetooth audio battery badge, and **APFS SSD free space**.
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
| **Hover over Dormant / Compact Bezel** | Opens Expanded Hub when Open Trigger is *Hover or Drag Down* or *Hover to Open* (configurable `0.05s – 0.75s`, default `0.09s`) |
| **Click & Drag Down from Notch** | Siri-style 1:1 pull-down gesture to open the Expanded Hub (*Hover or Drag Down* and *Drag Down (Like Siri)* modes) |
| **Drag Up toward Bezel** | Smoothly squeezes and collapses the Expanded Hub |
| **Click Bezel to Expand** | Optional single-click expansion toggle |
| **Two-Finger Horizontal Swipe** | Cycles tabs when Expanded; switches active Live Activities (*Media ↔ Timer*) or skips tracks (*Next / Previous*) when Compact |
| **Drag File Near Top Bezel** | Auto-expands the Shelf & AirDrop drop zones |
| **Pin Open Button** | Locks the Expanded Hub open across app switches until unpinned or collapsed |
| **App Switch / Fullscreen App** | Collapses automatically on outside app activation (and optionally auto-hides in fullscreen apps) |

### Menu Bar Keyboard Shortcuts
| Shortcut | Action |
| :--- | :--- |
| `⌘ I` | Enable / Disable Notch Island |
| `⌘ E` | Expand / Collapse Notch |
| `⌘ M` | Open Camera Mirror |
| `⌘ T` | Preview Volume HUD |
| `⌘ ,` | Settings… |
| `⌘ Q` | Quit Strata Notch |

---

## Customization & Themes

Open **Settings (`⌘,`)** or click the gear icon in the Expanded Hub header:

- **4 Visual Themes** (with interactive color swatch picker):
  - **Liquid Glass (macOS 26)** — Translucent specular glass with dynamic chroma refraction
  - **Pure Black (OLED)** — Deep pitch-black extension of the physical hardware notch
  - **Midnight Graphite** — Dark anodized space-black aluminum with subtle cool rim
  - **Arctic Frost** — Bright frosted silver-ice glass with crisp highlights
- **3 Bezel Shapes**: *Classic Notch Contour*, *Dynamic Island Pill* (automatically reserved on notchless displays, optional toggle for notched MacBooks), and *Minimal Drop*.
- **3 Rim Glow Styles**: *None (Pure Stealth)*, *Subtle Frost Rim*, and *Adaptive Activity Glow* (tints rim glow to active media artwork, timers, charging, or Keep Awake).
- **3 Compact Wing Detail Styles**: *Minimal Dots*, *Standard (Artwork + Bars)*, and *Rich (Track & Details)*.
- **3 Open Trigger Modes**: *Hover or Drag Down*, *Hover to Open*, and *Drag Down (Like Siri)*.
- **Geometry & Behavior**: Adjust notch width (`-40…+80 pt`) & height (`-8…+24 pt`) offsets, corner radius (`-4…+8 pt`), bezel opacity (`80%–100%`), hover expansion delay (`0.05s–0.75s`), click-to-expand, fullscreen auto-hide, track-change HUD pop-up, **Launch at Login** (`SMAppService`), and **drag-to-reorder Dock tabs**.
- **10 Active System Modules & 11 Modular Extensions**: Independently toggle every capability (Weather, Universal Now Playing, Hardware Volume/Brightness HUD, File Shelf, Camera Mirror, Timers/Pomodoro, System Telemetry, Clipboard & Scratchpad, Connectivity Alerts, Calendar Glance, Native HUD Suppression, Audio Waveform, Bluetooth 10-Band EQ, Bluetooth Battery Breakdown, SSD Disk Telemetry, CoreWLAN Wi-Fi Details, Focus Toggles, Notification Mirror, Downloads Watcher, Download Tracker Pop-Out Pill, and macOS Shortcuts Runner).
- **Backup & Restore**: **Export**, **Import**, or **Reset** all preferences as JSON (`StrataNotch-Preferences.json`).

---

## Permissions & Privacy

Strata Notch processes everything **locally on your Mac** with **no analytics, no telemetry, and no external accounts**. Permissions are only requested when you use or enable the corresponding module, and our non-nagging permission helper never repeatedly spams system dialogs:

| Permission | Used For |
| :--- | :--- |
| **Location Services** | Exact CoreLocation GPS coordinates for local Weather (falls back automatically to IP estimation or custom city) |
| **Accessibility** | Global media keys, native macOS Volume/Brightness HUD suppression, Control Center Focus fallback, and Notification Center banner mirroring |
| **Automation (Apple Events)** | Reading track metadata and controlling playback/seeking in Apple Music, Spotify, and supported web browsers |
| **Calendar** | Displaying upcoming meetings and 1-click Join links in Calendar Glance |
| **Camera** | Quick Camera Mirror preview (immediately stops hardware capture on collapse) |
| **Screen & System Audio Recording** | Optional real-time system audio FFT spectrum bars via ScreenCaptureKit (no screen pixels are stored or recorded) |

A built-in **Permissions & Media Diagnostics (`6/6 Ready`)** checklist in Settings lets you verify status at a glance, open the exact System Settings privacy pane, relaunch after granting Screen Recording, or click **Reveal App** if a duplicate copy in `/Applications` is competing with a development build.

---

## Requirements & Compatibility

- **macOS 15.0 (Sequoia)** or later *(macOS 26.0 Tahoe enables native Liquid Glass APIs)*
- **Apple Silicon (`arm64`)** & **Intel (`x86_64`)** Universal binary
- Works on MacBooks with a physical notch as well as notchless Macs and external monitors (automatic Dynamic Island Pill mode)

---

<div align="center">
  <p>Created by <strong>Chenitha Palugaswewa • Strata</strong></p>
  <p><sub>MIT License • © 2026 Chenitha Palugaswewa • All rights reserved.</sub></p>
</div>
