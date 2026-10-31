# sakti/tap

Homebrew tap and release downloads for Jejak, a desktop viewer for
OpenTelemetry traces, metrics and logs. Builds are for Apple silicon macOS
only.

## Install with Homebrew

```bash
brew tap sakti/tap
brew install sakti/tap/jejak
jejak --demo
```

Upgrade with `brew upgrade jejak`.

## Formulae

| Formula | Description                                               |
| ------- | --------------------------------------------------------- |
| `jejak` | Desktop viewer for OpenTelemetry traces, metrics and logs |

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
Jejak source repository. Do not edit `Formula/jejak.rb` by hand.
