# MMD Studio

> An MMD (MikuMikuDance) model viewer and animation editor for Android, with real-time 3D rendering and a native interface.

**English** · [简体中文](README.md)

---

## What it is

MMD Studio lets you open, tweak and record MMD models and motions right on your phone —
no desktop required, and no need to convert your project files first. It reads PMX / PMD
models and VMD motions directly, renders in real time, and saves what you see.

The renderer is built on Babylon.js, while the interface is drawn natively rather than
being a web page in a wrapper — so dragging a material slider has none of that
browser-like lag.

## Features

**Rendering**

- Full-screen real-time 3D, physics simulation and IK solving
- Material pipeline: subsurface scattering approximation, toon outline, rim light, emission, normal strength, per-material recolouring
- Grading: AgX tone mapping, ASC CDL, three-way colour grading, LUTs, white balance, split toning
- Post effects: bloom, ambient occlusion, depth of field, motion blur, film grain, vignette, chromatic aberration, sharpen
- Scene control: ground materials, skybox and environment maps, multiple lights, fog, ambient particles

**Editing**

- Model: import and remove, multiple models on stage, facial morphs, transform gizmo, position and scale nudging
- Motion: VMD playback, speed, range loop, frame stepping, motion blending, mirror, reverse, cross-fade
- Camera: view presets, camera path record and replay, field of view, gaze follow
- Scene: ground and sky, lighting and shadows, solid backdrop, Gaussian-splat stage

**Output**

- Screenshots (self-timer, burst, watermark)
- Screen recording
- Preset save, load, import and export
- GLB export

**Other**

- Bilingual UI (Simplified Chinese / English), following the system or set manually
- Light and dark themes
- Crash logs written to external storage for easy bug reports

## Download

Grab the latest package from the **[Releases](../../releases)** page.

| Item | Requirement |
|---|---|
| OS | Android 7.0 (API 24) or newer |
| Storage | "All files access" is requested on first launch, to scan for model and audio files |
| Network | Used only when checking for updates |

## Where to put your files

Follow this folder layout and the app will scan them automatically:

```
/storage/emulated/0/MMDStudio/
├── Models/   # PMX / PMD (keep textures alongside; relative paths resolve automatically)
├── Motions/  # VMD motions and camera data
└── Audios/   # MP3 / WAV / OGG / FLAC / M4A
```

## In-app updates

The app checks once shortly after launch (no more than once per 6 hours per device).
You can also check manually at **Mine → Updates → Check for updates**.

When a new version is available it downloads and installs right inside the app, with no
browser detour. Installing requires a one-time grant of "install unknown apps" — an
Android 8.0+ restriction that no third-party app can bypass.

## Feedback

Please open an [Issue](../../issues) and include:

- Device model and OS version
- What happened and how to reproduce it
- Crash logs from `Download/MMDStudio/crash/`, or in-app under **Mine → Crash logs**

> If the app dies instantly with no crash file at all, it is almost certainly a native
> crash in the WebGL / GPU driver while running the render process. Send the device
> model, and try updating the system WebView to the latest version.

---

**Note**: This project is not affiliated with Crypton Future Media or the official
MikuMikuDance. Please respect the licence terms of the models and motions you load.
