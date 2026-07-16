# pacman.zig

[![Build](https://github.com/floooh/pacman.zig/actions/workflows/main.yml/badge.svg)](https://github.com/floooh/pacman.zig/actions/workflows/main.yml)
[![WASM Demo](https://img.shields.io/badge/Demo-WASM-blue?style=flat-square&logo=webassembly)](https://floooh.github.io/pacman.zig/pacman.html)
[![Language-Zig](https://img.shields.io/badge/Language-Zig-F7A41D?style=flat-square&logo=zig)](https://ziglang.org/)

A Pac-Man 256 clone written in Zig using the Sokol headers for platform abstraction.

> **Play in Browser**: [WASM Demo](https://floooh.github.io/pacman.zig/pacman.html)

## 📖 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Build & Run](#build--run)
- [Build for WebAssembly](#build-for-webassembly)
- [Project Structure](#project-structure)
- [Controls](#controls)
- [Related Projects](#related-projects)
- [Contributing](#contributing)
- [Credits](#credits)

## Overview

This is a high-fidelity Zig port of the classic Pac-Man 256 endless scrolling arcade game. Built with modern Zig for safety and performance, it maintains lightweight, zero-dependency builds.

## Features

- 🎮 **Pac-Man 256 Gameplay** - Endless scrolling maze action
- 🌐 **Cross-Platform** - Runs on Windows, macOS, Linux, and WebAssembly
- ⚡ **Zero Dependencies** - Uses only Zig standard library and Sokol
- 🔧 **Modern Zig** - Built with Zig for performance and safety
- 🖼️ **Multiple Renderers** - D3D11 (Windows), OpenGL (Linux), Metal (macOS), WebGL2 (Web)

## Requirements

- [Zig](https://ziglang.org/) compiler (current development version recommended)
- Platform-specific dependencies:
  - **Windows**: D3D11
  - **Linux**: OpenGL, X11, ALSA development packages
  - **macOS**: Xcode Command Line Tools

## Build & Run

```bash
git clone https://github.com/Seaus-tech/PACMAN-ZIG
cd PACMAN-ZIG
zig build run
```

For release builds:
```bash
zig build --release=safe run
```

## Build for WebAssembly

> **NOTE**: This will install a local Emscripten SDK into the Zig cache, so the first run will take a while.

```bash
zig build -Dtarget=wasm32-emscripten run
```

For optimized web builds:
```bash
zig build -Dtarget=wasm32-emscripten --release=small run
```

## Project Structure

```
PACMAN-ZIG/
├── src/              # Zig source code
├── sokol/            # Sokol headers for graphics/audio/input
├── build.zig         # Zig build configuration
└── README.md         # This file
```

## Controls

- **Arrow Keys** - Move Pac-Man
- **Esc** - Exit

## Related Projects

- [**PACMAN-C**](https://github.com/Seaus-tech/PACMAN-C) - Original C99 implementation
- [**PACMAN256-C**](https://github.com/Seaus-tech/PACMAN256-C) - Pac-Man 256 in C
- [**PACMAN-256 (SwiftUI)**](https://github.com/Seaus-tech/PACMAN-256) - Native iOS/macOS port

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Credits

- **Sokol**: https://github.com/floooh/sokol
- **Original Pac-Man**: Namco, 1980

© 2026 Seaus Tech. All rights reserved.