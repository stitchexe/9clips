# 9clips

Instant replay for Windows games. 9clips keeps the last minute of your screen and sound in memory while you play,
and saves it as a clip when you press a key. Then browse your clips, and cut, trim and join them in the built-in editor.

**[Download the latest version](https://github.com/stitchexe/9clips/releases/latest)**: the installer
(`9clips-x.y.z-setup.exe`) or, if you'd rather not install anything, the zip (`9clips-x.y.z-win64.zip`).

## What you need

- Windows 10 (version 1903 or newer) or Windows 11, 64-bit
- An NVIDIA graphics card (GeForce GTX 900 series or newer) with a current driver: 9clips records on its built-in
  video encoder (NVENC), so it barely touches your frame rate
- FFmpeg, a free video tool. The first time 9clips runs it offers to download it for you (about 110 MB, gyan.dev's
  build, checked against its published checksum).

## What it does

- **Instant replay:** press **Alt+F10** to save the last 60 seconds (anything from 10 s to 20 min), sorted into a
  folder per game. **Alt+F8** saves just the last 30 s, **Alt+F1** takes a screenshot.
- **Recording:** **Alt+F9** records to disk for as long as you like while instant replay keeps going. A recording
  survives a crash, a full disk or a Windows shutdown.
- **True 60 fps clips** with Windows Graphics Capture, in H.264, HEVC or AV1.
- **Audio:** game sound plus your microphone, mixed or as separate tracks, with noise suppression for the mic.
  Optionally the game, other apps (music, voice chat) and the mic each get their own track.
- **Clips browser:** thumbnails that scrub on hover, search, favorites, a filter by game, and an optional size
  cap that clears out the oldest clips.
- **Editor:** a frame-accurate timeline with filmstrip and waveform. Split, trim, delete and rearrange parts; splice
  in parts of other clips; mute the mic or turn tracks up and down. Export an exact cut, an instant fast cut, a
  Discord-sized file (10, 25 or 50 MB), a GIF, or just the audio.
- **Your look:** themes, any accent color, any font, and your own wallpaper.
- **Stays out of the way:** it lives in the tray. Closing the window keeps recording.

Measured on an RTX 5070 Ti and a Ryzen 7 5700X3D while recording 1080p60: about 0.4% CPU, 1.3% GPU, 140 MB of RAM
for a 60 s buffer, and about 3% lower FPS in a GPU-heavy test with the Light capture method (9% with Smooth).

## Installing

- **Installer:** run `9clips-x.y.z-setup.exe`. It installs for your Windows account only (no admin rights needed),
  adds 9clips to the Start menu and, if you like, starts it with Windows. Uninstall it from Apps & features; your
  clips and settings stay.
- **Zip:** unzip it anywhere and run `9clips.exe`.

### "Windows protected your PC"

9clips isn't code-signed yet, so Windows SmartScreen doesn't recognize it. Click **More info**, then **Run anyway**.
If Smart App Control is turned on, Windows blocks unsigned apps entirely and 9clips can't run.

## Getting started

| Key | What it does |
|-----|--------------|
| Alt + F10 | save the last 60 seconds |
| Alt + F8 | save the last 30 seconds |
| Alt + F9 | start or stop a recording |
| Alt + F1 | take a screenshot |

Change the keys, the clip length and the quality in Settings. NVIDIA's own overlay (GeForce Experience or the NVIDIA
app) uses some of the same keys; if one doesn't work, 9clips tells you: turn off NVIDIA's instant replay or pick
other keys.

## Privacy

9clips collects nothing about you or your clips. It goes online only to:

- ask GitHub once a day whether a newer version is out (turn it off in Settings > General), and
- download FFmpeg, when you say so.

## Where things are

| | |
|---|---|
| Clips | `Videos\9clips` (change it in Settings) |
| Settings | `%APPDATA%\9clips` |
| Log and the downloaded FFmpeg | `%LOCALAPPDATA%\9clips` |

## Problems?

[Open an issue](https://github.com/stitchexe/9clips/issues) and attach the log (`%LOCALAPPDATA%\9clips\9clips.log`;
Settings > General > Open log folder).

## License

9clips is free to use; see [LICENSE.txt](LICENSE.txt). It records with [FFmpeg](https://ffmpeg.org), which it doesn't
include and downloads only when you ask: gyan.dev's build, under the GNU GPL v3.
