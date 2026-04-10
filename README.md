# zig-raylib-template

A minimal Zig + Raylib starter project.

- Zig module-based build (`build.zig`)
- Raylib pulled via `build.zig.zon` dependency
- Simple example in `src/main.zig` that opens a window and clears the background

## Requirements

- Zig `0.15.2+` (this repo sets `.minimum_zig_version = "0.15.2"` in `build.zig.zon`)

## Quick start

Build:
- `zig build`

Run:
- `zig build run`

## Project layout

- `src/main.zig` — small example program using `@cImport` with:
  - `raylib.h`
  - `raymath.h`
- `build.zig` — builds the executable and links the Raylib artifact from the dependency
- `build.zig.zon` — pins Raylib as a dependency

## Raylib version / pinning note

This template pins Raylib to a specific commit:

- `git+https://github.com/raysan5/raylib#efda35b309e012dda56288072d4de57448f85fd0`

The pin is intentional: Raylib’s `master` can move quickly, and at times Zig tooling (e.g. ZLS) may not match the exact Zig dev version required by Raylib at HEAD. Pinning keeps the template stable and reproducible.
