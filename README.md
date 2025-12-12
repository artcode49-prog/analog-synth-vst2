# artcode SYNTH

Analog-style synthesizer VST3/CLAP plugin built with Rust and nih-plug.

## Features

- **Dual Oscillators** - Two independent oscillators with Sin/Saw/Sqr/Tri waveforms
- **Filter** - Low Pass / High Pass / Band Pass with resonance and envelope modulation
- **Drive** - Warm saturation/distortion
- **ADSR Envelope** - Attack, Decay, Sustain, Release
- **LFO** - Modulates Pitch, Filter, or Amplitude
- **Portamento** - Smooth pitch glide
- **Arpeggiator** - Up/Down/Up-Down/Random with selectable speed and octave range
- **Effects** - Delay and Reverb
- **50+ Factory Presets** - Bass, Lead, Pad, Keys, Pluck, FX categories
- **User Presets** - Save your own presets with custom names
- **16-voice Polyphony**

## Build

### Prerequisites

Install Rust from https://rustup.rs/

### Download Assets (Local Build Only)

Before building locally, download the UI assets:

```bash
mkdir -p assets
curl -L -o assets/knob.png "https://raw.githubusercontent.com/artcode49-prog/artcode/main/KNOB_blue.png"
curl -L -o assets/sidewood.png "https://raw.githubusercontent.com/artcode49-prog/artcode/main/sidewood.png"
curl -L -o assets/logo.png "https://raw.githubusercontent.com/artcode49-prog/artcode/main/artcodeSYNTH.png"
```

*Note: GitHub Actions automatically downloads assets during CI build.*

### macOS

```bash
cargo xtask bundle analog_synth --release
# Or: ./build-mac.sh
```

### Windows

```powershell
cargo xtask bundle analog_synth --release
# Or double-click: build-windows.bat
```

### Linux

```bash
cargo xtask bundle analog_synth --release
```

## Install

### macOS
```bash
cp -R "target/bundled/artcode SYNTH.vst3" ~/Library/Audio/Plug-Ins/VST3/
```

### Windows
```powershell
copy "target\bundled\artcode SYNTH.vst3" "C:\Program Files\Common Files\VST3\"
```

### Linux
```bash
cp -R "target/bundled/artcode SYNTH.vst3" ~/.vst3/
```

## Preset Categories

| Category | Count | Description |
|----------|-------|-------------|
| Init | 1 | Default sound |
| Bass | 10 | Fat Bass, Sub, Acid, Wobble, Reese, etc. |
| Lead | 10 | Sync, Screamer, Trance, Hoover, etc. |
| Pad | 10 | Soft, Warm, Strings, Choir, etc. |
| Keys | 9 | E.Piano, Organ, Clav, Bell, etc. |
| Pluck | 5 | Pluck, Guitar, Harp, etc. |
| FX | 5 | Rise, Laser, Siren, etc. |
| User | ∞ | Your saved presets |

## System Requirements

- **macOS**: 10.13+ (Intel or Apple Silicon)
- **Windows**: 10/11 (64-bit)
- **Linux**: Any modern distribution

## License

MIT
