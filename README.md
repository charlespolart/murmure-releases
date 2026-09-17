# Murmure

**Local, offline voice dictation for Mac.** Press a key, talk, release: your words are typed where your cursor is. Everything runs on your Mac — the audio never leaves it.

[**Download the latest version (DMG)**](https://github.com/charlespolart/murmure-releases/releases/latest/download/Murmure.dmg) · [All releases](https://github.com/charlespolart/murmure-releases/releases) · [Release notes](CHANGELOG.md)

This repository only hosts the **binaries** and the **update feed**. The source code is private.

## What it does

- **Dictate anywhere** with a global shortcut (or the Fn / Globe key), in any app. Hands-free mode available.
- **On-device transcription** with Whisper (WhisperKit), automatic language detection, French / English / Chinese and more.
- **Styles**: raw, clean, formal, concise, e-mail — or your own custom styles — applied on your Mac by a local language model.
- **Translate** or **restyle** any selected text from the menu.
- **Personal dictionary** so names and jargon come out right.
- **History** with audio playback and one-click re-run.
- Menu bar app: a small pill at the bottom of the screen, or a Dynamic Island–style notch on MacBooks.

## Requirements

- macOS **14 Sonoma** or later.
- **Apple Silicon** (M1 or later). Intel Macs are not supported.
- About 1 GB of free disk space for the speech model, downloaded on first launch. Optional cleanup models (for styles) are downloaded on demand.

## Install

1. Download `Murmure.dmg` and open it.
2. Drag **Murmure** to **Applications**, then launch it.
3. Follow the short onboarding: microphone access, accessibility permission (needed to type the text for you), model download.

The app is signed with an Apple Developer ID and notarized by Apple: it opens without any Gatekeeper workaround. To verify a download:

```sh
spctl --assess --type open --context context:primary-signature -v Murmure.dmg
```

## Updates

Murmure checks for updates automatically once a day, quietly: when a new version is available, a badge appears on the menu bar icon and the menu offers **Update to X.Y.Z…**. Updates are signed (EdDSA) and installed only when you ask. You can also pick **Check for Updates…** at any time.

Update feed (Sparkle appcast): `https://raw.githubusercontent.com/charlespolart/murmure-releases/master/appcast.xml`

## Privacy

- Audio is processed on your Mac and never uploaded.
- Nothing is sent anywhere by default. If you *choose* to configure a cloud style with your own API key, only the transcribed text is sent — never the audio, never your dictionary.
- Dictation history stays in your user folder; audio retention is a setting.

## Problems and feedback

Open an issue in this repository, or write to the author via [charlespolart.com](https://charlespolart.com).
