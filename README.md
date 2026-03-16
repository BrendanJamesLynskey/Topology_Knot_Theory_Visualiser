# Topology & Knot Theory Visualiser

An interactive single-file HTML application for exploring surfaces, knots, and topological invariants through 3D visualisations.

## Features

### 1. Surface Gallery
- **3D wireframe renderings** of classical surfaces using perspective projection on HTML5 Canvas
- Surfaces included: Mobius strip, Klein bottle, Torus, Sphere, Cross-cap (Real Projective Plane)
- Click-and-drag rotation, scroll-to-zoom
- Adjustable parameters (e.g., torus R/r ratio, Mobius twist count)
- Properties displayed: Euler characteristic, orientability, genus, boundary info

### 2. Euler Characteristic Calculator
- **Interactive simplicial complex editor** on a 2D canvas
- Click to add vertices, Shift+click two vertices to add edges, Ctrl+click inside a triangle to add faces
- Right-click to delete vertices
- Real-time computation and display of V - E + F = chi
- Preset examples: Tetrahedron, Cube, Octahedron, Torus triangulation

### 3. Knot Explorer
- **3D knot renderings** with depth-based crossing visualisation (over/under clearly shown)
- Common knots: Trefoil (3_1), Figure-Eight (4_1), Cinquefoil (5_1)
- Torus knot T(p,q) with adjustable p and q parameters
- Knot invariants displayed: crossing number, unknotting number, Alexander polynomial
- Rainbow color gradient along the knot curve for visual clarity

### 4. Fundamental Polygons
- **Edge identification diagrams** showing how surfaces are built from squares
- Surfaces: Torus (aba^{-1}b^{-1}), Klein bottle (abab^{-1}), RP^2 (abab), Sphere
- Animated folding/gluing process
- Adjustable animation speed

## Usage

Open `index.html` in any modern web browser. No build step or server required.

The only external dependency is Google Fonts (DM Sans, JetBrains Mono) loaded via CDN.

## Technical Details

- Pure vanilla JavaScript, HTML5 Canvas
- No WebGL -- all 3D rendering uses software perspective projection
- Wireframe rendering with depth-based alpha for visual depth cues
- Knot crossings rendered via depth-sorted segments with dark outlines
- Dark theme matching the project's math visualiser aesthetic

## Controls

| Action | Surface Gallery / Knot Explorer | Euler Calculator |
|--------|--------------------------------|------------------|
| Left-click + drag | Rotate 3D view | Add vertex |
| Scroll wheel | Zoom in/out | -- |
| Shift + click | -- | Add edge (click two vertices) |
| Ctrl/Cmd + click | -- | Add face (click inside triangle) |
| Right-click | -- | Delete vertex |
