<h1 align="center">
  <b>CrèmeNX</b>
  <br>
  <sub>A Nintendo Switch emulator for Android</sub>
</h1>

> [!WARNING]
> **CrèmeNX is in a rough, early state.** This is experimental software. Expect crashes, black screens, games that refuse to boot, missing features, and rough edges throughout the UI. It is not a polished, daily-driver emulator, and it is not ready for a general audience yet. If you are looking for something stable, this is not it — at least not yet.

## What this is

CrèmeNX is a fork of [Kenji-NX](https://git.ryujinx.app/projects/Kenji-NX), which itself descends from [Ryubing](https://git.ryujinx.app/projects/Ryubing) and, ultimately, the original Ryujinx emulator created by gdkchan. The emulation core is the same C# codebase those projects are built on; what CrèmeNX changes is mostly the Android front-end wrapped around it.

The menu layout and settings screens are heavily **inspired by [MeloNX](https://git.ryujinx.app/projects/MeloNX)** — the segmented Library/Settings header, the sidebar-driven settings pages, and the general look and feel all take their cues from it.

## Platforms

**Android only, for now.** This is the only platform that is built and tested today.

**iOS support is planned**, but it will be built on a **different core** rather than the one used here — the current core's approach does not translate to iOS. There is no timeline for this, and nothing to install or test yet.

## Screenshots

<p align="center">
  <img src="img/library_menu.jpg" alt="CrèmeNX game library" width="80%">
  <br>
  <em>The game library.</em>
</p>

<p align="center">
  <img src="img/settings_menu.jpg" alt="CrèmeNX graphics settings" width="80%">
  <br>
  <em>Settings, with the graphics page open.</em>
</p>

## Games and keys

CrèmeNX ships with no game content and no system files. You need to supply your own firmware, keys, and games, dumped from hardware you own. Please don't ask for these — they will not be provided here.

## Troubleshooting

Given how early this build is, things *will* go wrong. If you hit a problem, please report it — bug reports are genuinely useful right now.

**Get in touch:**

- **Discord:** DM **`twistedfeels`**
- **Telegram:** [join the group](https://t.me/+l0dNvVTtnHIxZmNk)

### Before you report

Please grab your logs — a report with a log attached is worth ten without one. You'll find them on your device at:

```
Android/data/com.angel.cremenx/files/Logs/
```

Two things live in there:

- `Ryujinx_1.0.0_<date>_<time>.log` — the regular log for each run. Attach the one matching the run that went wrong.
- `crash.log` — written when the app crashes outright. If it exists, include it.

When reporting, it helps a lot to also mention:

- Your **device and Android version** (both are shown at the top of the Settings page).
- The **game** you were running, if any.
- **What you did** and what happened instead — "black screen after the intro" beats "doesn't work".
- Any **settings you changed** from the defaults.

### Known rough edges

- Many games don't boot, hang on a black screen, or stall on a loading screen. Compatibility is inconsistent and varies title to title.
- Performance is not representative of what the emulator could do; don't judge it by this build.
- If the app misbehaves after an update, try clearing the app's data — but note this wipes your firmware, keys, and game folder settings, so back up `Android/data/com.angel.cremenx/files` first.

## Credits

CrèmeNX would not exist without the work of others:

- **[Ryujinx](https://git.ryujinx.app/archive/ryujinx-mirror)** by gdkchan and contributors — the original emulator this all descends from.
- **[Ryubing](https://git.ryujinx.app/projects/Ryubing)** — the fork that carried the project forward.
- **[Kenji-NX](https://git.ryujinx.app/projects/Kenji-NX)** — the direct upstream of this fork, and the source of the emulation core and Android bindings.
- **[MeloNX](https://git.ryujinx.app/projects/MeloNX)** — the inspiration for the menu layout and settings design.

## License

CrèmeNX is released under the [MIT license](LICENSE.txt), matching its upstream. Portions of the code are copyright the Kenji-NX Team, the Ryujinx contributors, and their respective authors.
