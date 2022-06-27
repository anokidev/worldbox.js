<div style="display: flex; justify-content: center;" align="center">
<h1>WorldBox</h1>
</div>

This repository is used to host the source code of WorldBox.js, a free and open source 
Javascript library for creating live 2D and 3D graphics using Canvas API nor WebGL.

## How to install:

Run this command:

```bash
npm install -g worldbox # Install WorldBox globally.
npm install worldbox # Install WorldBox locally.
```

Then after that, you can import WorldBox staight into your javascript files:

```javascript

// Import line.
import canvas from "worldbox";

/* CANVAS */

// Create a new canvas.
const cvs = new canvas(document.querySelector("#canvas"), "3d");

/* RENDERER CONFIGURATION */

// Choose your renderer.
const renderer = new cvs.render("webgl");

// Set your renderer pixel ratio.
renderer.setPixelRatio(window.devicePixelRatio);

/* WORLD */

// Create a new world.
const world = new cvs.world("infinite");

/* CAMERA CONFIGURATION */

// Choose your camera.
const camera = new cvs.new("camera", [10, 10, 10]);

// Set your camera type to perspective.
camera.setType("perspective");

// Set your camera FOV.
camera.setFOV(window.innerWidth / window.innerHeight);

/* SKYBOX */

// Create a new box.
const box = new cvs.shape("box", [0, 0, 0]);

// Set size.
box.setSize("world");

// Set fill type.
box.setFillType("transparent");

// Set fill color.
box.setFillColor("#12b7e0");

/* INIT */

// Render.
renderer.init();

```