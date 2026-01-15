# Perlin-Noise-Contours Shader

A procedural shader creating smooth, animated contour lines using Perlin noise. Multiple line frequencies are layered to produce visually appealing flowing patterns.

## Features

- Smooth, animated lines using Perlin noise as a scalar field
- Branchless, GPU-friendly rendering using `fract` and `step`
- Adjustable line thickness and resolution
- Multiple contour frequencies (major/minor lines)
- Fully customizable colors
- Easy to integrate into ShaderToy or other GLSL environments

## How It Works

1. Generate a smooth scalar field using Perlin noise in 2D + time.
2. Multiply by a resolution factor and compute `fract(band / N)` to create repeating bands.
3. Use `step` as a branchless threshold to define line masks.
4. Blend multiple frequencies/colors with `mix` for layered contours.
5. Animate over time by feeding `iTime` into the noise function.

## Usage

- Copy the `mainImage` function into your GLSL environment (ShaderToy, Shadertoy-compatible editor, or WebGL/GLSL project).
- Adjust `RESOLUTION` and `thickness` to control line density and width.
- Change `N` values and colors to create your own contour hierarchy.

## Live Demo

- ShaderToy: https://www.shadertoy.com/view/WX3czl

## License

MIT License
