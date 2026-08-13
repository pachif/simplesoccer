# 🏆 WORLD CUP SOCCER — Retro Remake

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange.svg)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![No Dependencies](https://img.shields.io/badge/Dependencies-None-brightgreen.svg)](#)
[![Retro Style](https://img.shields.io/badge/Style-Retro_8bit-purple.svg)](#)

> **Relive the golden age of arcade football!** A pure vanilla JavaScript homage to classic 16-bit World Cup soccer games, featuring authentic retro visuals, CRT scanline effects, and fast-paced 2-minute matches.

![Game Screenshot](https://via.placeholder.com/480x426/000000/FFFFFF?text=Retro+Soccer+Gameplay)

---

## ⚡ Features

### 🎮 Gameplay
- **8 Playable National Teams** with unique attributes (Speed, Power, Defense):
  - 🇧🇷 Brazil | 🇩🇪 W. Germany | 🇦🇷 Argentina | 🇮🇹 Italy
  - 🏴󠁧󠁢󠁥󠁮󠁧󠁿 England | 🇫🇷 France | 🇪🇸 Spain | 🇯🇵 Japan
- **Arcade Matches**: Fast-paced 2-minute games with **Golden Goal** sudden death
- **CPU Difficulty Levels**: Low, Average, and High (affects AI reaction, speed, and accuracy)
- **Dynamic Kit System**: Away teams automatically change kits to avoid color clashes
- **Team Mentality**: Offensive or defensive playstyles derived from team stats

### 📺 Visuals & Audio
- **CRT Scanline Effect**: Authentic retro monitor simulation with vignette
- **Pixel-Perfect Rendering**: Canvas rendering with `image-rendering: pixelated`
- **Procedural Graphics**: All sprites and animations drawn via Canvas API (no external assets)
- **Web Audio API**: Synthesized sound effects for kicks, goals, and whistles
- **Responsive Design**: Scales to any screen size while maintaining aspect ratio

### 📱 Controls
- **Keyboard**: Arrow keys + Z/X/C (or WASD + J/K/L)
- **Touch Controls**: On-screen D-Pad and A/B buttons for mobile devices
- **Auto-Detection**: Touch controls appear only on touch-enabled devices

---

## 🚀 Quick Start

### Option 1: Play Immediately
Simply open `index.html` in any modern web browser. No installation required!

```bash
# Using Python's built-in server
python3 -m http.server 8000
# Then visit http://localhost:8000
```

### Option 2: Local Development
```bash
# Clone the repository
git clone <your-repo-url>
cd world-cup-soccer

# Open in browser
open index.html  # macOS
xdg-open index.html  # Linux
start index.html  # Windows
```

---

## 🎯 How to Play

### Controls
| Action | Keyboard | Touch |
|--------|----------|-------|
| Move Player | Arrow Keys / WASD | D-Pad |
| Pass / Tackle | Z / J | Button B |
| Shoot / Sprint | X / K | Button A |
| Pause / Start | Enter / C / L | Start Button |

### Game Modes
1. **Exhibition Match**: Pick your team and face off against CPU
2. **Tournament Mode**: *(Coming soon)* Complete bracket-style tournament

### Tips
- **Golden Goal**: In knockout stages, the first goal wins instantly!
- **Team Chemistry**: Choose teams that match your playstyle (e.g., Brazil for offense, Italy for defense)
- **Master the Timing**: Perfect your shots and tackles to beat higher difficulties

---

## 🛠️ Technical Details

### Architecture
- **Single File**: Entire game logic, rendering, and styles in one `index.html` file
- **Vanilla JavaScript**: No frameworks, no build tools, no dependencies
- **Canvas 2D API**: All graphics rendered procedurally using `ctx.fillRect`, `ctx.arc`, etc.
- **Game Loop**: `requestAnimationFrame` for smooth 60 FPS animation
- **State Machine**: Menu → Team Select → Match → Results flow

### Key Systems
```javascript
// CPU Difficulty Configuration
const DIFFS = [
  { name: 'LOW',     spd: .82, react: .45, steal: .25, err: 1.5 },
  { name: 'AVERAGE', spd: 1.0,  react: 1.0,  steal: .45, err: 1.0 },
  { name: 'HIGH',    spd: 1.12, react: 1.6,  steal: .62, err: .6 }
];

// Team Attributes (Speed, Power, Defense multipliers)
const TEAMS = [
  { name: 'BRAZIL',   spd: 1.06, pow: 1.05, def: 0.95 },
  { name: 'ITALY',    spd: 0.96, pow: 0.95, def: 1.12 },
  // ... 6 more teams
];
```

### Browser Compatibility
- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Android)

---

## 📜 License

This project is licensed under the **GNU General Public License v3.0** (GPL-3.0).  
See the [LICENSE](LICENSE) file for details.

**You are free to:**
- Share and adapt the code
- Use it for personal or commercial projects
- Modify and distribute derivatives

**Under these terms:**
- Derivative works must also be licensed under GPL-3.0
- Include copyright notice and license text
- Disclose source code when distributing binaries

---

## 🤝 Contributing

Contributions are welcome! Since this is a single-file project, please:

1. **Fork** the repository
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Make your changes** (keep the single-file structure if possible)
4. **Test thoroughly** across different browsers
5. **Commit** your changes (`git commit -m 'Add amazing feature'`)
6. **Push** to the branch (`git push origin feature/amazing-feature`)
7. **Open a Pull Request**

### Code Style Guidelines
- Use ES6+ features (const/let, arrow functions, template literals)
- Keep functions small and focused
- Comment complex game logic (AI behavior, physics calculations)
- Maintain retro aesthetic (no modern UI elements)

---

## 🙏 Acknowledgments

- Inspired by classic **World Cup Soccer** games from the 16-bit era
- Font: **[Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P)** by Cody "CodeMan38" Boisclair
- Built with ❤️ using pure **HTML5 Canvas** and **JavaScript**

---

## 📬 Contact

Have questions, suggestions, or found a bug?  
Open an issue on GitHub or reach out to the community!

---

<div align="center">

**⚽ Kick off the nostalgia! ⚽**

*Made for retro gaming enthusiasts everywhere*

</div>
