# Subway Chase 3D

A lightweight, browser-based 3D endless runner built with **Three.js**. This project is a functional clone of the popular *Subway Surfers* game, featuring 3D model loading, lane-based movement, and a procedural power-up system.

---

## 🚀 Features

* **3D Graphics:** Powered by the Three.js WebGL engine.
* **Dynamic Asset Loading:** Loads external `.glb` models for characters (Jake, Inspector), trains, and items.
* **Animation System:** Supports skeleton-based animations (Run, Jump, Fly) and procedural "bobbing" animations.
* **Power-ups:**
    * **Coins:** Increase your total score.
    * **Boots:** Temporary jump height boost.
    * **Jetpack/Hoverboard:** Activates "Fly Mode" to soar above obstacles.
* **Adaptive Difficulty:** Game speed increases gradually the further you run.
* **Retro Audio:** Synthesized 8-bit sound effects and background music using the Web Audio API.

---

## 🎮 How to Play

The goal is simple: **Run as far as you can without hitting a train.**

| Action | Key |
| :--- | :--- |
| **Move Left** | `A` or `Left Arrow` |
| **Move Right** | `D` or `Right Arrow` |
| **Jump** | `Space` |

---

## 🛠️ Technical Stack

* **Engine:** [Three.js](https://threejs.org/) (R128)
* **Model Loader:** GLTFLoader
* **Styling:** CSS3 for UI overlays and menus
* **Audio:** Native Web Audio API (Oscillators)

---

## 📦 Setup & Installation

Since this is a single-file HTML project, no complex installation is required:

1.  Clone or download the `index.html` file.
2.  Open the file in any modern web browser (Chrome, Firefox, Edge).
3.  **Note:** Because the game fetches 3D assets from GitHub via HTTPS, an active internet connection is required to load the models.

---

## 📂 Project Structure

* **Model Loading:** Assets are managed through an `assetsToLoad` array with custom offsets and scales to ensure different models fit the game world.
* **Collision Logic:** Uses `THREE.Box3` for bounding box intersection checks with "forgiving" hitboxes (scalar expansion) for better gameplay feel.
* **Object Pooling:** Procedural generation creates "rows" of obstacles and items at `Z = -80` and cleans them up once they pass the camera to save memory.
