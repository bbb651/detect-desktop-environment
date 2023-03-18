# Detect Desktop Environment

[![GitHub](https://img.shields.io/badge/GitHub-demurgos%2Fdetect-desktop-environment-informational.svg)](https://github.com/demurgos/detect-desktop-environment)
[![crates.io](https://img.shields.io/crates/v/detect-desktop-environment.svg?maxAge=86400)](https://crates.io/crates/detect-desktop-environment)
[![CI status](https://img.shields.io/github/workflow/status/demurgos/detect-desktop-environment/check-rs/main)](https://github.com/demurgos/detect-desktop-environment/actions/workflows/check-rs.yml)
[![docs.rs/detect-desktop-environment](https://img.shields.io/crates/v/detect-desktop-environment.svg?maxAge=86400)](https://docs.rs/detect-desktop-environment)

This crate helps you to detect the current desktop environment.
It was inspired by the [`detectDE`](https://cgit.freedesktop.org/xdg/xdg-utils/tree/scripts/xdg-utils-common.in?h=fa5805559ad27382ef62110cb23e67d6eb649030#n270)
function from _xdg-util_.

## Installation

Run the following command in your project:
```
cargo add detect-desktop-environment
```

## Usage

```rust
use detect_desktop_environment::DesktopEnvironment;

fn main() {
    match DesktopEnvironment::detect() {
        Some(de) => println!("detected desktop environment: {de:?}"),
        None => println!("failed to detect desktop environment"),
    }
}
```

This library exposes two symbols: the `detect` function and it returns value: the
`DesktopValue` enum. All the variants are listed below in the "Supported environments"
section.

## Supported environments

| Name            | Thumbnail                                        |
|-----------------|--------------------------------------------------|
| `Cinnamon`      | ![Cinnamon](./thumbnails/cinnamon.png)           |
| `Cosmic`        | ![COSMIC](./thumbnails/cosmic.png)               |
| `Enlightenment` | ![Enlightenment](./thumbnails/enlightenment.png) |
| `Gnome`         | ![Gnome](./thumbnails/gnome.png)                 |
| `Kde`           | ![Kde](./thumbnails/kde.png)                     |
| `Lxde`          | ![Lxde](./thumbnails/lxde.png)                   |
| `Lxqt`          | ![Lxqt](./thumbnails/lxqt.png)                   |
| `MacOs`         | ![MacOs](./thumbnails/mac-os.png)                |
| `Mate`          | ![Mate](./thumbnails/mate.png)                   |
| `Unity`         | ![Unity](./thumbnails/unity.png)                 |
| `Windows`       | ![Windows](./thumbnails/windows.png)             |
| `Xfce`          | ![Xfce](./thumbnails/xfce.png)                   |

# Documentation

See [docs.rs/detect-desktop-environment](https://docs.rs/detect-desktop-environment).

# Maintenance status

This library is stable and no major changes are expected.

If you want to improve the library, feel free to open an issue or send a PR. Breaking changes are allowed.
Note however that review times may be slow.

# Minimum Supported Rust Version (MSRV) policy

The last 8 stable versions are explicitly supported (1 year). See [Cargo.toml](./Cargo.toml) for details.

# License

[MIT](./LICENSE.md)
