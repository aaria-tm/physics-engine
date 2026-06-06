# physics-engine
# Interactive Physics Sandbox

A single-file, web-based physics engine laboratory designed to visually demonstrate fundamental physics concepts. Built with vanilla JavaScript, **Matter.js** for robust rigid-body physics, and **Tailwind CSS** for a clean, modern user interface.

## Features
* **Zero Setup Required:** Runs entirely in the browser. No build steps, no servers, and no installations necessary.
* **Multi-Concept Scene Manager:** Dynamically clears and rebuilds the physics world based on the selected educational topic.
* **Interactive UI:** Click buttons to apply forces, fire projectiles, and drop objects in real-time.
* **Educational Display:** Shows the title, description, relevant formula, and variable breakdown for each selected concept.

## 🛠️ Tech Stack
* **HTML5 Canvas:** The rendering surface for the simulation.
* **Vanilla JavaScript:** Handles the scene management, UI logic, and user interactions.
* **[Matter.js](https://brm.io/matter-js/):** The 2D physics engine handling collisions, mass, gravity, and restitution.
* **[Tailwind CSS](https://tailwindcss.com/):** Handles all styling via CDN for a sleek, dark-mode design.

---

## How to Run

1. Create a new folder on your computer (e.g., `PhysicsSandbox`).
2. Download or copy the code into a file named `sandbox.html`.
3. Double-click `sandbox.html` to open it in any modern web browser (Chrome, Firefox, Safari, Edge).
4. *Note: You must have an active internet connection the first time you open it so the browser can fetch the Matter.js and Tailwind CSS libraries.*

---

## Concepts Covered

The sandbox includes 5 distinct scenes, each isolating a specific physics principle:

### 1. Newton's 2nd Law ($F = ma$)
Demonstrates inertia. Applies the exact same force to a light box and a heavy box to show how mass inversely affects acceleration.

### 2. Conservation of Momentum ($p = mv$)
Simulates a top-down, zero-gravity environment. Fire a heavy, fast-moving projectile into a stationary target to observe the transfer of kinetic energy and momentum.

### 3. Friction ($F_f = \mu F_n$)
Spawns identical boxes on three different surfaces: Ice (low friction), Wood (medium friction), and Rubber (high friction). Applies identical impulses to show how surface resistance affects sliding distance.

### 4. Gravity & Free Fall ($d = \frac{1}{2}gt^2$)
Disables air resistance (a true vacuum). Drops a massive object and a tiny object simultaneously to prove that gravity accelerates all masses at the exact same rate.

### 5. Restitution ($e = v_{after} / v_{before}$)
Drops three objects with different bounciness coefficients (0.2, 0.6, and 1.0) onto a static floor to demonstrate inelastic versus perfectly elastic collisions.

---

## How to Expand / Customize

Because this is a single-file application, you can easily tweak the physics parameters by editing the `concepts` object inside the `<script>` tag.

* **Want to change gravity?** Find `engine.world.gravity.y = 1;` and increase the number.
* **Want to add more objects?** Look at the `setup()` function inside any concept and duplicate the `Bodies.rectangle()` or `Bodies.circle()` lines.
* **Want to change colors?** Update the `fillStyle` hex codes (e.g., `#3B82F6` for blue).

## 📝 License
This project is completely open-source and free to use for educational purposes, personal projects, or classrooms.
