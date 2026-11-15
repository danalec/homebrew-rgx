# homebrew-rgx

A personal Homebrew **tap** for [rgx](https://github.com/danalec/rgx):
search inside everything — PDFs, Office documents, archives, 3D models, LLM
checkpoints, databases, e-mail and media metadata, with ripgrep's interface.

This is NOT Homebrew/homebrew-core. The formula here is maintained by the
rgx project itself and installs the prebuilt macOS archives from the rgx
GitHub release; nothing is submitted to Homebrew's own repository.

## Install

```sh
brew tap danalec/rgx
brew install rgx
```

The tap name is `danalec/rgx` because Homebrew strips the `homebrew-`
prefix from `danalec/homebrew-rgx`.

## What it installs

`rgx`, the same binary the crates.io package `rgx-search` and the Windows /
Linux installers ship. Both Apple silicon and Intel Macs are supported,
pinned to the SHA256 of their release archives.

## Updating

The canonical formula lives in the rgx repository at `Formula/rgx.rb`. On a
new release, `scripts/push-github.sh` rewrites its version, URLs and digests
from the macOS archives it publishes, and `scripts/publish-homebrew.sh`
(`.ps1` on Windows) copies the rewritten file here. This tap is a
distribution point, not a second source of truth.
