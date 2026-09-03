# Voicebox Qwen M4

Apple Silicon build overlay for [jamiepine/voicebox](https://github.com/jamiepine/voicebox), pinned to upstream commit `51f49dea198384b4eb6087b72c17057c6eb1c1cd`.

## Download

- [Voicebox-Qwen-M4.dmg](https://github.com/l3snikk/voicebox-qwen-m4/releases/download/v0.1.0/Voicebox-Qwen-M4.dmg) — recommended installer
- [Voicebox-Qwen-M4.app.zip](https://github.com/l3snikk/voicebox-qwen-m4/releases/download/v0.1.0/Voicebox-Qwen-M4.app.zip) — application bundle
- [Release v0.1.0](https://github.com/l3snikk/voicebox-qwen-m4/releases/tag/v0.1.0)

## Install on Apple Silicon

1. Download and open the DMG.
2. Drag **Voicebox Qwen M4** to **Applications**.
3. On the first launch, Control-click the app, choose **Open**, then confirm.

The build is ad-hoc signed and integrity-checked, but not notarized by Apple. If macOS still blocks it, verify that the file came from this repository and run:

```bash
xattr -dr com.apple.quarantine "/Applications/Voicebox Qwen M4.app"
```

Model weights are downloaded by Voicebox on first use and are not bundled.

## Included

- MLX single-worker fix from PR #989
- MLX and voice-prompt memory cleanup from PR #1074
- Qwen EOS/runaway protection from PR #1078
- conservative Qwen leading-artifact cleanup adapted from PR #1048
- 600 ms paragraph pauses
- Qwen 1.7B/0.6B-only TTS selector, Russian by default
- Whisper support
- official auto-updates disabled for this custom build

The Actions workflow builds on a native GitHub ARM64 macOS runner, runs the Qwen/MLX regression tests, creates an ad-hoc-signed `.app` and DMG, and verifies the application signature.
