# SwiftFlash GUI

> **Looking for SwiftFlash?** The actively developed tool is the
> [SwiftFlash command-line app](https://github.com/zehrer/SwiftFlash). This repository holds an earlier
> SwiftUI app that is not maintained at the moment.

## SwiftFlash (command line)

[SwiftFlash](https://github.com/zehrer/SwiftFlash) flashes `.img` / `.iso` images to SD cards and USB sticks on
macOS. Images can be local files, `.xz` compressed, or loaded from an `http(s)` URL or a registered build server.
It is a single native Swift binary that uses only system frameworks.

```bash
brew install zehrer/tap/swiftflash
swiftflash id                                   # which image is on the card (read-only)
sudo swiftflash ~/Downloads/image.img.xz        # flash, choosing the card interactively
```

Requires an Apple Silicon Mac with macOS 13 or later. See the
[SwiftFlash README](https://github.com/zehrer/SwiftFlash#readme) for all commands.

### Shared formats

SwiftFlash defines formats that a future GUI is meant to share, so both tools can work with the same media
and settings. This app does not use them yet:

- [`/.uuid` metadata file](https://github.com/zehrer/SwiftFlash/blob/main/docs/uuid-file.md): identifies the
  medium and the flashed image.
- `~/.swiftflash/config.json`: media inventory, remembered images, flash history and image sources.
- [Publishing images](https://github.com/zehrer/SwiftFlash/blob/main/docs/build-server.md): what a build
  server should provide.

## This app

A native SwiftUI app (macOS 15.6+) with drag and drop, a device inventory, a privileged helper for writing,
and `.iso`, `.img` and `.img.xz` support. Features, build instructions, design principles and testing notes:
[docs/app-details.md](docs/app-details.md).

## License

MIT. See [LICENSE](LICENSE).
