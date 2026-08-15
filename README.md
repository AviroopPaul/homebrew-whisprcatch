# WhisprCatch Homebrew tap

Homebrew cask for [WhisprCatch](https://github.com/AviroopPaul/whisper-catch) —
local push-to-talk dictation for macOS. Hold a key, speak, release; punctuated
text is typed wherever your cursor is. Runs 100% on-device.

```sh
brew install --cask AviroopPaul/whisprcatch/whisprcatch
```

Apple Silicon, macOS 11+.

## After installing

WhisprCatch needs three macOS permissions before it can hear the push-to-talk
key and type for you. Open it once and the first-run wizard walks you through:

| Permission | Why |
| --- | --- |
| Accessibility | types transcribed text into the focused app |
| Input Monitoring | notices the push-to-talk key globally |
| Microphone | captures speech while the key is held |

macOS only re-reads these when an app starts, so after granting them quit
WhisprCatch and open it again. `whisper-catch doctor` prints their live status.

## Note on signing

WhisprCatch is signed with its own certificate rather than an Apple Developer
ID, so the cask clears the download's quarantine flag after Homebrew has
verified it against the published checksum. This is also what keeps your
granted permissions from resetting on every update.

---

This repository is generated — the cask is maintained at
[`packaging/homebrew/whisprcatch.rb`](https://github.com/AviroopPaul/whisper-catch/blob/main/packaging/homebrew/whisprcatch.rb)
in the main repo and pushed here by CI on release.
