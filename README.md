# Voicebox Qwen M4

Apple Silicon build overlay for [jamiepine/voicebox](https://github.com/jamiepine/voicebox), pinned to upstream commit `51f49dea198384b4eb6087b72c17057c6eb1c1cd`.

Included:

- MLX single-worker fix from PR #989
- MLX and voice-prompt memory cleanup from PR #1074
- Qwen EOS/runaway protection from PR #1078
- conservative Qwen leading-artifact cleanup adapted from PR #1048
- 600 ms paragraph pauses
- Qwen 1.7B/0.6B-only TTS selector, Russian by default
- Whisper support
- official auto-updates disabled for this custom build

The Actions workflow creates an ad-hoc-signed `.app` and `.dmg`. Model weights are downloaded by Voicebox at runtime and are not bundled.
