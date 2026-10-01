# 🦖 hamid-ne9az — Dino Jump Game

A Chrome Dino-style endless runner game built with pure HTML, CSS, and JavaScript. No libraries, no build step — just open and play!

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

🎮 **Live Demo:** https://hamidPC-molpc.github.io/hamid-ne9az/ *(after enabling Pages, see below)*

## ✨ Features

- 🏃 Animated dino with running legs
- 🌵 4 random cactus obstacle types (small, medium, large, wide)
- ☁️ Scrolling clouds and ground details
- ⚡ Progressive difficulty — speeds up every 500 points
- 🏆 Score tracking + high score
- 📱 Responsive canvas (800x300), keyboard + click/tap support
- 📦 Zero dependencies — single HTML file

## 🚀 How to Play

### Play online
Open `https://hamidPC-molpc.github.io/hamid-ne9az/` in any browser.

### Play locally
1. Clone the repo:
   ```bash
   git clone https://github.com/hamidPC-molpc/hamid-ne9az.git
   cd hamid-ne9az
   ```
2. Open `index.html` (or `dino-game.html`) in your browser — double-click works.
   - Or serve it: `npx serve .` or `python -m http.server`

### Controls
- **SPACE** — Start / Jump / Restart
- **Mouse Click / Tap** — Start / Jump / Restart

Avoid the cacti! Each frame survived = 1 point.

## 🛠️ Tech Stack

- HTML5 Canvas for rendering
- Vanilla CSS for layout
- Vanilla JavaScript for game loop (`requestAnimationFrame`), physics (gravity, jump velocity), collision detection (AABB), and spawning

## 📁 Project Structure

```
hamid-ne9az/
├── index.html        # Playable game (GitHub Pages entry point)
├── dino-game.html    # Original game file (same as index.html)
├── README.md         # This file
├── LICENSE          # MIT License
└── .gitignore
```

## ⚙️ Game Tuning

Want it easier/harder? Edit these in `index.html`:

```js
let gameSpeed = 6;        // starting speed
gravity: 0.8,             // fall speed
jumpForce: -15,           // jump height
if (score % 500 === 0) {
  gameSpeed += 0.5;       // difficulty ramp
}
```

## 🌐 Enable GitHub Pages

1. Go to repo **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** / **(root)**
4. Save — game will be live in ~1 min at the URL above.

Or via CLI:
```bash
gh api repos/hamidPC-molpc/hamid-ne9az/pages -f build_type=legacy -f source='{"branch":"main","path":"/"}'
```

## 📝 License

MIT — see [LICENSE](LICENSE). Free to use, modify, and share.

## 🙏 Credits

Inspired by Chrome's offline `chrome://dino` runner. Built from scratch with Canvas.
