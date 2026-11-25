# Hexa

A music player for Android that hands your audio to the hardware instead of the mixer.

**[Support, feedback and bug reports → Telegram](https://t.me/HexaPlayerSupport)**

This is the first beta. If something sounds wrong, skips, or an album shows up oddly,
please say so in the group — the phone model and what you played is usually enough to
track it down.

---

## High-resolution output, not high-resolution marketing

Most Android players hand your music to the system mixer, and the mixer resamples it to
whatever the phone happens to be doing at that moment. A 24-bit / 96 kHz file quietly comes
out at 48 kHz, and nothing on screen tells you it happened.

Hexa can take a different route. On supported devices it plays through a **Direct Thread**
or **MMAP Exclusive** path that steps around the mixer entirely, so the file reaches the
hardware at its own sample rate and bit depth. No hidden resampling, no silent conversion
to whatever the system felt like today.

That is the whole point of the app. Everything else exists so this part can work.

And when a phone doesn't allow it, Hexa says so. The output screen always reports the path,
rate and depth that were **actually used** for the track playing — not the ones that were
requested. If your phone caps direct output at 48 kHz, you will see 48 kHz and know it is
the phone's limit rather than guessing at the player's.

## What it is

Hexa plays your local music files. It reads what Android already indexes, and can also pull
in folders that Android skips, so a library of FLAC, ALAC, APE or DSD files is playable
without converting anything first.

It is built around one idea: hand audio to the device as directly as the device allows, and
otherwise stay quiet. Where a phone supports a direct path, Hexa uses it; where it doesn't,
Hexa plays through the normal mixer rather than pretending otherwise.

## Features

- **High-resolution output.** Direct Thread or MMAP Exclusive on supported devices, taking
  the system mixer out of the signal path so music plays at its own rate and depth.
- **Honest output reporting.** The rate, bit depth and output path shown are the ones really
  in use, per track — so you always know what reached the hardware.
- **Plays almost anything.** A built-in decoder handles FLAC, ALAC, APE, WavPack, AIFF,
  Opus, AAC, MP3 and DSD, with Android's own decoder as a fallback.
- **A library that matches how you think.** Songs, albums, artists and folders, with search
  across all of it.
- **Full artwork.** Cover art is shown at full resolution in the player, uncropped.
- **Folders Android ignores.** Add a folder and Hexa will index formats the system scanner
  skips.
- **Material 3 design**, with light and dark themes that follow your system colours.
- **No account, no tracking, no internet.** The app does not request internet permission at
  all — it cannot send anything anywhere.

## Install

1. Download the latest APK from [Releases](../../releases).
2. Open it. Android will ask permission to install from this source; allow it.
3. Play Protect may offer to scan the app, because it has not seen this one before.
   "Install without scanning" is fine.

Requires Android 8.0 or newer on a 64-bit device.

**Updating from an earlier build:** this release is signed with Hexa's own key, so a build
signed with a different key cannot be installed over it. If Android refuses the update,
uninstall the old app first. That is a one-time step.

## A note on what your phone allows

What Hexa can do depends on the phone, not on the app. Some devices allow Direct Thread or
MMAP Exclusive output at high sample rates and bit depths; others cap it at 48 kHz, and some
only expose a path the system mixer resamples anyway. Hexa does not hide that — the output
screen shows exactly what happened for the track you are playing.

## Feedback

Bugs, requests and "this sounds wrong on my phone" all belong in the
[Telegram group](https://t.me/HexaPlayerSupport). When reporting a playback problem, the
Output settings page is the most useful thing to include — it says which path was used and
at what rate.
