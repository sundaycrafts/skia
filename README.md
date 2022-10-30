Skia is a complete 2D graphic library for drawing Text, Geometries, and Images.

See full details, and build instructions, at https://skia.org.

## Setup

### Download Source

The official document recommends using depot_tools that originally for dealing with Chromium development to download.
Basically, it's a collection of scripts but also download development tools such as Python, [GN](https://gn.googlesource.com/gn/), git (if it's not installed yet).

See [How to download Skia | Skia](https://skia.org/docs/user/download/) for detail.

## Getting Started (Tutorial)

### Build Skia Viewer

Skia Viewer demonstrate basic Skia features. It's built using regular GN process.

```sh
# for M1 mac
gn gen out/Release --args='is_debug=false target_cpu="arm64"'
ninja -C out/Release viewer
```

| Key   | Action                                                |
|-------|-------------------------------------------------------|
| ← →   | Move between the slides                               |
| ↑ ↓   | Zoom in / out                                         |
| d     | Change render methods among raster, OpenGL and Vulkan |
| s     | Display rendering times and graph                     |
| Space | Toggle display of Tools UI                            |

- [Skia Viewer | Skia](https://skia.org/docs/user/sample/viewer/)

### Build Other testing apps

```sh
# After `gn gen`
ninja -C out/Release HelloWorld
```

See [./BUILD.gn](./BUILD.gn) for more options.
