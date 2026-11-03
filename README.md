# sakti/tap

Homebrew tap and release downloads for Jejak, a desktop viewer for
OpenTelemetry traces, metrics and logs, and DuckPlus, a native IDE for DuckDB
over the Quack protocol. Homebrew installs are for Apple silicon macOS only.
DuckPlus also has a Windows download.

## Install with Homebrew

```bash
brew tap sakti/tap
brew install sakti/tap/jejak
jejak --demo
```

Upgrade with `brew upgrade jejak`.

```bash
brew install --cask sakti/tap/duckplus
```

Upgrade with `brew upgrade --cask duckplus`.

## Formulae

| Formula | Description                                               |
| ------- | --------------------------------------------------------- |
| `jejak` | Desktop viewer for OpenTelemetry traces, metrics and logs |

## Casks

| Cask       | Description                                   |
| ---------- | --------------------------------------------- |
| `duckplus` | Native IDE for DuckDB over the Quack protocol |

## Download

Each [release](https://github.com/sakti/homebrew-tap/releases) has a
`.tar.gz` archive for Apple silicon Macs (`aarch64-apple-darwin`) and a
`SHA256SUMS` file. Intel Macs are not supported.

The binaries are not notarized. If you download an archive with a browser,
macOS quarantines it; remove the quarantine before the first run:

```bash
xattr -d com.apple.quarantine jejak
```

Homebrew installs do not need this step.

DuckPlus releases are tagged `duckplus-v<version>`. Each has a `.zip` for Apple
silicon Macs (`aarch64-apple-darwin`), a `.zip` for Windows
(`x86_64-pc-windows-msvc`) and a `SHA256SUMS` file. The builds are not signed,
so Windows may show a SmartScreen warning. If you download the macOS zip with a
browser, remove the quarantine before the first run:

```bash
xattr -dr com.apple.quarantine DuckPlus.app
```

## Moved from sakti/jejak-release

This repository was `sakti/jejak-release`. If you installed Jejak from the
old tap, change to the new one:

```bash
brew uninstall jejak
brew untap sakti/jejak-release
brew tap sakti/tap
brew install sakti/tap/jejak
```

## Maintenance

This repository is updated automatically when a version is tagged in the
Jejak or DuckPlus source repository. Do not edit `Formula/jejak.rb` or
`Casks/duckplus.rb` by hand.
