# 🌐 PolySphere — My First Three.js Project

This is a simple yet visually engaging 3D visualization built using **Three.js**. It's my first exploration into the world of WebGL and 3D rendering in the browser. The core shape is an **icosahedron** wrapped in a wireframe, giving it a sleek geometric aesthetic that you can rotate and explore interactively.

<img width="1912" height="955" alt="image" src="https://github.com/user-attachments/assets/651f29f3-177d-4114-bd82-9e8a29df511e" />


---

## 🚀 Live Demo
[Demo](https://poly-sphere.netlify.app/)

---

## 🛠️ Technologies Used
- [Three.js](https://threejs.org/)
- JavaScript (ES6+)
- HTML5 / CSS3
- WebGL (via Three.js)
- OrbitControls

---

## 💡 What I Learned

As this is my **first Three.js** project, here are some of the core concepts I explored and learned:

### 📌 Three.js Basics
- **Scene, Camera, Renderer:** The foundational elements of any Three.js app.
- **PerspectiveCamera:** Mimics the human eye with adjustable field of view, aspect ratio, and clipping planes.
- **WebGLRenderer:** Renders the 3D content onto the HTML `<canvas>` using WebGL.

### 🧱 Geometry & Materials
- **IcosahedronGeometry:** A built-in Three.js geometry made up of 20 triangular faces — perfect for low-poly style.
- **MeshStandardMaterial:** A physically-based material that reacts to lighting and gives the shape a realistic finish.
- **Wireframe Overlay:** Added a `MeshBasicMaterial` with `wireframe: true` to layer a geometric mesh for style and clarity.

### 🔧 Controls
- **OrbitControls:** Let the user interactively rotate, zoom, and pan the camera around the object with smooth damping.

### 🌗 Lighting
- **HemisphereLight:** Simulates indirect lighting from above and below, giving the object a more natural ambient glow.

### 🧩 Responsive Design
- Learned how to handle **window resizing** to keep the canvas full-screen and responsive:
  ```js
  window.addEventListener('resize', () => {
    camera.aspect = window.innerWidth / window.innerHeight;
    camera.updateProjectionMatrix();
    renderer.setSize(window.innerWidth, window.innerHeight);
  });
