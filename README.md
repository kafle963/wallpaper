# Drift — Interactive Apple Lock Screen & Spotify Lyrics Wallpaper

A minimal, glassmorphic interactive Windows desktop wallpaper featuring dynamic sky time-of-day transitions, Apple Music & Spotify Canvas style synced background lyrics with progressive fluid word sweep and dynamic album auroras, cute headphones desktop cat companion, Apple Lock Screen style typography with custom greetings, and live Spotify Desktop playback integration.

## 🎵 Dynamic Synced Lyrics & Music Experience

### How it Works
- **Apple Music Fluid Word Sweep**: Active lyrics progressively fill with glowing light across the text from left to right as the words are sung.
- **Dynamic Dual-Orb Album Auroras**: Automatically extracts vibrant dominant colors from the current album cover and casts an ambient breathing color aura behind the lyrics.
- **3D Depth-of-Field Stage**: Previous and upcoming lyric lines smoothly blur and scale down, keeping the current active line in razor-sharp focus.
- **Instrumental 7-Bar Equalizer**: Harmonic animated multi-bar equalizer wave displays during guitar solos and beat drops.
- **Timing Sync Calibration Slider**: Real-time offset slider (`-4.0s` to `+4.0s`) in Settings to micro-tune lyrics sync to your exact system/audio setup.
- **Headphones Vibing Desktop Cat**: The desktop cat puts on glowing headphones, bops along with the music rhythm, and emits ambient floating iridescent music bubbles.
- **Smart Active Widget**: Clean glassmorphism player with vinyl rotation, seeker bar, and media controls.

### 2 Easy Ways to Connect Spotify:

#### Method 1: Spotify Web API (Direct API with Full Controls)
1. In the wallpaper Settings gear (`⚙`), paste your **Client ID** and click **Connect with Spotify**.
2. This redirects to `spotify_connect.html` where you can 1-click authorize.
3. In your [Spotify Developer Dashboard](https://developer.spotify.com/dashboard), ensure your App's **Redirect URIs** includes the URL shown on `spotify_connect.html`.
4. Click **Authorize with Spotify**.
5. Once authorized, your permanent **Refresh Token** is saved automatically and redirects back to `index.html`!
6. Once connected, the settings panel shows a clean **● Spotify Connected** badge and provides an **Advanced Settings** dropdown for setup changes or disconnecting.

> ⚠️ **Staying connected across reboots:** Lively's built-in web renderer clears the browser's local storage every time Lively restarts (this is a known Lively limitation, not specific to this wallpaper), so a Spotify connection saved only in the browser can ask you to reconnect after a reboot. To make it permanent, open **Advanced Spotify Settings** in the panel, tap **Copy** next to your Client ID and Refresh Token, then right-click the wallpaper → **Customize** and paste them into the matching **Spotify Client ID** / **Spotify Refresh Token** fields there. Lively saves those fields to its own settings file on disk, so they survive every future restart automatically — no more reconnecting.

#### Method 2: Lively Wallpaper (Zero Setup)
If you run this wallpaper inside **Lively Wallpaper** on Windows:
- Open the Spotify Desktop app and play any song.
- Lively Wallpaper will automatically pipe Windows system media track data directly to the wallpaper widget!

---

## ✨ Features
- **Apple Music Studio Synced Lyrics**: Dynamic gradient word fill sweep, dual-orb album color auroras, depth blur, and jump-to-timestamp interaction.
- **Headphones Vibing Desktop Cat**: Interactive cute desktop companion that bops to the beat and reacts to petting and clicks.
- **Ultra-Smooth Spotify Glass Player**: Draggable anywhere on the desktop, zero-lag 60fps seek bar, vinyl rotation, shuffle, repeat, and play/pause controls.
- **Apple Lock Screen Clock & Typographic Styles**: Switch between Glassy Frosted Apple Lock mode and Solid high-contrast mode.
- **Dynamic Time of Day**: Morning, Afternoon, Sunset Evening, and Starry Night (7:00 PM – 11:59 PM) with twinkling stars and moon.
- **Settings Panel (`⚙`)**: Live settings to adjust font sizes, lyrics offset calibration, time of day, text opacity, and Spotify API configuration.

## 🚀 Usage
Open [index.html](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html) in any modern browser, or load it into **Lively Wallpaper** on Windows.
