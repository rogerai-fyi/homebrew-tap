# homebrew-tap

Homebrew tap for [**RogerAI**](https://rogerai.fyi) — a two-way radio for GPUs.

## Install

Homebrew 6+ requires you to trust a third-party tap once before it will load the tap's
code, so install is a single copy-paste line:

```sh
brew trust rogerai-fyi/homebrew-tap && brew install rogerai-fyi/homebrew-tap/roger
```

Then run `roger`. Works on **macOS and Linux**, Apple Silicon and Intel (arm64 + amd64).

Upgrade later with `brew update && brew upgrade roger`; remove with `brew uninstall roger`.

> Not on `brew install roger` with no tap? That requires homebrew-core, which only accepts
> OSI-approved licenses — RogerAI is source-available under PolyForm Perimeter, so a tap is
> the supported route.

## What's here

`Formula/roger.rb` installs the prebuilt `roger` binary from the matching
[GitHub release](https://github.com/rogerai-fyi/roger/releases). It's **generated**, not
hand-written: [`scripts/gen-brew-formula.sh`](https://github.com/rogerai-fyi/roger/blob/main/scripts/gen-brew-formula.sh)
renders it from each release's `checksums.txt`, and the `roger` repo's release workflow
pushes it here automatically on every `v*` tag. Don't edit it by hand — your change will be
overwritten on the next release.
