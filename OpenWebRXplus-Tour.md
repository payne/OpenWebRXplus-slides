---
marp: true
theme: default
paginate: true
backgroundColor: #1a1a2e
color: #eaeaea
style: |
  section {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  h1 {
    color: #00d4ff;
  }
  h2 {
    color: #00d4ff;
  }
  a {
    color: #ff6b6b;
  }
  code {
    background-color: #16213e;
  }
  section.title {
    text-align: center;
  }
  section.title h1 {
    font-size: 2.5em;
  }
  img[alt~="center"] {
    display: block;
    margin: 0 auto;
  }
  table {
    background-color: transparent;
  }
  th {
    background-color: transparent;
    border-bottom: 2px solid #00d4ff;
  }
  td {
    background-color: transparent;
  }
  tr {
    background-color: transparent;
  }
  tr:nth-child(even) {
    background-color: rgba(255, 255, 255, 0.05);
  }
---

<!-- _class: title -->

# OpenWebRX+

## A Tour of the Web-Based Software Defined Radio

**Your Browser is Now a Radio Receiver**

Built: BUILD_TIMESTAMP
https://github.com/payne/OpenWebRXplus-slides

---

# What is OpenWebRX+?

- **Web-based SDR receiver** accessible from any modern browser
- **Multi-user** - many listeners can tune simultaneously
- **No client software** - just open a URL and start listening
- **Open source** fork with enhanced features
- Works with affordable hardware like RTL-SDR (~$30)

> "Listen to radio signals from anywhere in the world through your browser"

---

# Why OpenWebRX+?

| Traditional Radio | OpenWebRX+ |
|-------------------|------------|
| Physical hardware required | Browser only |
| One user at a time | Multiple simultaneous users |
| Limited to your location | Access receivers worldwide |
| Manual tuning | Click-to-tune interface |
| Expensive equipment | $30 SDR dongle |

---

# The Web Interface

## Main Components

- **Waterfall Display** - Visual representation of signals over time
- **Spectrum Display** - Real-time signal strength graph
- **Tuning Panel** - Frequency, mode, and bandwidth controls
- **Audio Controls** - Volume, squelch, noise reduction
- **Bookmark Bar** - Quick access to saved frequencies

---

# Waterfall Display

The waterfall shows radio activity as a scrolling image:

- **Horizontal axis** = Frequency
- **Vertical axis** = Time (scrolling down)
- **Color intensity** = Signal strength

**Interaction:**
- Click anywhere to tune
- Drag to pan across the band
- Scroll to zoom in/out
- Touch-friendly for mobile devices

---

# Supported Modes - Analog

## Voice & Audio

| Mode | Description |
|------|-------------|
| **AM** | Amplitude Modulation (broadcast radio) |
| **FM** | Frequency Modulation (VHF/UHF) |
| **WFM** | Wideband FM (commercial broadcast) |
| **USB/LSB** | Single Sideband (amateur radio) |
| **CW** | Continuous Wave (Morse code) |
| **SAM** | Synchronous AM (improved AM reception) |

---

# Supported Modes - Digital Voice

## Talk Digital

| Mode | Description |
|------|-------------|
| **DMR** | Digital Mobile Radio |
| **D-Star** | Amateur digital voice |
| **YSF** | Yaesu System Fusion |
| **NXDN** | Kenwood/Icom digital |
| **FreeDV** | Open source digital voice |

*Requires compatible codec libraries*

---

# Supported Modes - Data

## Weak Signal & Data Modes

| Mode | Use Case |
|------|----------|
| **FT8/FT4** | Weak signal amateur contacts |
| **WSPR** | Propagation beacon monitoring |
| **JT65/JT9** | EME and weak signal work |
| **JS8Call** | Keyboard-to-keyboard chat |
| **PSK31/63** | Digital text modes |

---

# Aviation Decoders

## Track Aircraft in Real-Time

- **ADS-B** - Aircraft position and identification
- **ACARS** - Aircraft text messaging system
- **HFDL** - HF Data Link communications
- **VDL2** - VHF Data Link Mode 2

Decoded aircraft appear on the built-in map!

---

# Maritime & Paging

## More Specialized Decoders

**Maritime:**
- **AIS** - Ship identification and tracking

**Paging Systems:**
- **POCSAG** - Pager messages
- **FLEX** - Advanced paging protocol

**Selective Calling:**
- DTMF, EEA, EIA, CCIR, ZVEY variants

---

# Image Modes

## Pictures Over Radio

- **SSTV** - Slow Scan Television
  - Background decoding while you listen
  - Multiple SSTV formats supported

- **FAX** - Weather Facsimile
  - Decode weather maps from marine broadcasts
  - Automatic image assembly

---

# CW Skimmer

## Decode All Morse Code Simultaneously

- Monitors entire 48kHz bandwidth
- Detects and decodes all CW signals at once
- Displays callsigns and frequencies in real-time
- Great for contest monitoring or band activity

---

# Interactive Maps

## Visualize the Radio World

The built-in map displays:

- **Aircraft positions** (from ADS-B decoding)
- **Ship locations** (from AIS decoding)
- **APRS stations** (amateur radio tracking)
- **Other public WebSDRs** worldwide
- **HAM repeater locations**
- **Shortwave broadcaster sites**

---

# Bookmarks & Scanning

## Never Miss a Signal

**Bookmarks:**
- Save favorite frequencies with labels
- Organize by category
- Click to instantly tune

**Scanner:**
- Automatically scan through bookmarks
- Stop on active signals
- Resume scanning after activity stops

---

# Audio Features

## Crystal Clear Reception

- **Noise Reduction** - Spectral subtraction filtering
- **Squelch** - Silence when no signal
- **Audio Recording** - Save what you hear
- **Multiple Sample Rates** - Balance quality vs bandwidth

---

# Multi-User Features

## Share the Experience

- **Simultaneous Users** - Many listeners, one receiver
- **Built-in Chat** - Talk with other listeners
- **User Presence** - See who's connected
- **Admin Controls** - Manage connections

---

# User Awareness

## Who Else is Listening?

**What regular users see:**
- **Client count** in status bar (e.g., "Clients [5]")
- **Chat messages** from other users with nicknames and colors
- Warning when connections near capacity (85%)

**Admin-only visibility:**
- Detailed client list with IPs and connection times
- Which SDR/profile each user is on
- Ability to disconnect problem users

---

# Built-in Chat

## Real-Time Communication

- Choose a nickname when you connect
- System assigns you a unique color
- Messages broadcast to all connected users
- Timestamps on all messages

Great for。
- Asking "What frequency is that signal?"
- Sharing interesting finds
-。ordinating during events or contests

---

# Bookmark Types

## Three Scopes of Bookmarks

| Type | Color | Who Owns It | Storage |
|------|-------|-------------|---------|
| **Local** | Blue | You (per browser) | Browser localStorage |
| **Server** | Yellow | Administrator | Server config files |
| **Bandplan** | Green | System-generated | Auto from databases |

**Your local bookmarks are private and independent!**

---

# Per-User Bookmarks

## Your Bookmarks Stay With You

- Stored in your browser's localStorage
- Never sent to the server
- Create, edit, delete freely
- Survive page refreshes

**Limitation:**
- Tied to browser/device, not an account
- Won't sync across your devices
- Clearing browser cache deletes them

---

# Independent Tuning

## Can Multiple Users Tune Differently?

**Yes!** Each user can tune to a different frequency within the SDR's bandwidth.

```
┌─────────────────────────────────────────────────┐
│           SDR Bandwidth (e.g., 500 kHz)         │
│                                                 │
│  User A        User B        User C            │
│    ▼             ▼             ▼               │
│ 145.75 MHz   146.00 MHz   146.52 MHz           │
│ (Repeater)   (Simplex)    (Calling)            │
└─────────────────────────────────────────────────┘
```

All three listen simultaneously and independently!

---

# How Independent Tuning Works

## Bandwidth Sharing Architecture

**Shared by all users:**
- Center frequency (e.g., 146.00 MHz)
- Total bandwidth (determined by sample rate)
- The raw RF signal from the SDR

**Independent per user:**
- Frequency offset within bandwidth
- Modulation mode (FM, SSB, AM, etc.)
- Bandwidth/filter settings
- Squelch level
- Audio processing

---

# Independent Tuning Example

## 2-Meter HAM Band Scenario

SDR configured: **Center 146.00 MHz, 500 kHz bandwidth**

| User | Listening To | Offset | Mode |
|------|--------------|--------|------|
| Alice | 145.75 MHz repeater | -250 kHz | FM |
| Bob | 146.52 simplex | +520 kHz | FM |
| Carol | 144.39 APRS | -1.61 MHz | **Out of range!** |

Carol would need a different SDR profile to reach 144.39 MHz.

---

# The Bandwidth Constraint

## What Users Share

- Changing the **center frequency** affects everyone
- Switching **receiver profiles** affects everyone
- You can only tune within the current bandwidth window

**Think of it like cable TV:**
- One cable brings in a range of channels
- Each viewer picks their channel from what's available
- Can't watch channels outside the package

---

# Supported Hardware

## From Budget to Professional

| Device | Price Range | Notes |
|--------|-------------|-------|
| RTL-SDR | $30 | Great starter, 24MHz-1.7GHz |
| Airspy | $170-300 | Better sensitivity |
| SDRPlay | $100-250 | Wide frequency coverage |
| HackRF | $300 | TX capable, very wide range |
| Perseus | $1000+ | Professional HF receiver |

---

# Deployment Options

## Run It Your Way

1. **Raspberry Pi** - Dedicated low-power receiver
   - Pre-built SD card images available
   - Pi 3B+ minimum for digital voice

2. **Linux Server** - Full power setup
   - Debian/Ubuntu packages available

3. **Docker** - Containerized deployment
   - x86-64, ARM64, ARM32 support

---

# Architecture Overview

```
┌─────────────┐     ┌──────────────┐     ┌─────────────┐
│  SDR Device │────▶│  OpenWebRX+  │────▶│   Browser   │
│  (Hardware) │     │   (Server)   │     │  (Client)   │
└─────────────┘     └──────────────┘     └─────────────┘
                           │
                    ┌──────┴──────┐
                    │   Decoders  │
                    │  (csdr/dsp) │
                    └─────────────┘
```

- Python backend with signal processing
- WebSocket for real-time data
- Web Audio API for playback

---

# Configuration

## Key Settings

```
# Network
port: 8073
bind_address: 0.0.0.0

# Receiver
sdr_device: rtlsdr
frequency_offset: 0

# Features
enable_adsb: true
enable_aprs: true
```

Web-based admin panel for most settings!

---

# Reporting & Integration

## Connect to the World

- **PSKReporter** - Share decoded FT8/WSPR spots
- **WSPRnet** - Contribute to propagation database
- **MQTT** - Send data to home automation
- **APRS-IS** - Connect to APRS network

---

# Plugin System

## Extend the Functionality

Available plugins include:
- Enhanced S-Meter display
- Colorized spectrum
- Bookmark search
- Antenna switching
- Doppler tracking (satellite)
- Custom map layers

---

# Getting Started

## Quick Start Steps

1. **Install** - Use package manager or Docker
   ```bash
   docker pull slechev/openwebrxplus
   ```

2. **Configure** - Set up your SDR device

3. **Access** - Open `http://your-server:8073`

4. **Tune** - Click the waterfall and listen!

---

# Resources

## Learn More

- **Website:** https://www.openwebrx.de/
- **GitHub:** https://github.com/luarvique/openwebrx
- **Plugins:** https://github.com/0xAF/openwebrxplus-plugins
- **Wiki:** Comprehensive setup guides
- **Public Receivers:** http://rx.linkfanel.net/

---

<!-- _class: title -->

# Questions?

## Try a Public Receiver Now!

Visit any public OpenWebRX+ instance and start exploring the radio spectrum

**http://rx.linkfanel.net/**

---

# Thank You!

## Key Takeaways

- Browser-based SDR - no software installation
- 40+ decoders for voice, data, and images
- Works with affordable hardware
- Multi-user and globally accessible
- Active open-source community

**Happy Listening!**
