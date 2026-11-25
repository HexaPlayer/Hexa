# Hexa

A music player for Android that tries to stay out of the way of the music.

**[Support, feedback and bug reports → Telegram](https://t.me/HexaPlayerSupport)**

This is the first beta. If something sounds wrong, skips, or an album shows up oddly,
please say so in the group — a short description of the phone and what you played is
usually enough to track it down.

---

## What it is

Hexa plays your local music files. It reads what Android already indexes, and can also
pull in folders that Android skips, so a library of FLAC, ALAC, APE or DSD files is
playable without converting anything first.

It is built around one idea: the player should hand audio to the device as directly as
the device allows, and otherwise stay quiet. Where a phone supports a direct output path,
Hexa uses it; where it doesn't, Hexa plays through the normal mixer rather than pretending
otherwise. The settings show what your phone actually did.

## Features

- **Plays almost anything.** A built-in decoder handles FLAC, ALAC, APE, WavPack, AIFF,
  Opus, AAC, MP3 and DSD, with Android's own decoder as a fallback.
- **Direct output where supported.** On phones that allow it, audio skips the system mixer
  instead of being resampled on the way out.
- **Honest output settings.** Sample rate and bit depth are chosen per track, and the
  screen tells you what is really playing rather than what was asked for.
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

## A note on sound quality

What Hexa can do depends on your phone, not on the app. Some devices allow direct output at
high sample rates and bit depths; others cap it at 48 kHz, and some only expose a path the
system mixer resamples anyway. The output screen in Settings reports exactly what happened
for the track you are playing, so you can see whether the limit is the phone or the file.

## Feedback

Bugs, requests and "this sounds wrong on my phone" all belong in the
[Telegram group](https://t.me/HexaPlayerSupport). When reporting a playback problem, the
Output settings page is the most useful thing to include — it says which path was used and
at what rate.
