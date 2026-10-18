# How to move a Frog

<div align="center">

🐸 How to move a Frog V1.0 (Froggers Extrem)

Web-based Match-3 Arcade Hybrid & Amiga Retro Engine

English Version | Deutsche Version

</div>

<!--
ENGLISH SECTION
Standard for GitHub projects. Focuses on technical vocabulary.
-->

🔧 Overview

**How to move a Frog** (also known as *Froggers Extrem*) is a web-based retro arcade hybrid that fuses tactical Match-3 puzzle mechanics with the classic Frogger gameplay, built in the aesthetic of a 16-Bit Amiga application.

The project explores a unique design question: *How do you control a frog when every step requires dedicated directional energy?* Instead of free movement, players must clear direction tiles on a puzzle board to earn movement points for Up, Down, Left, and Right. The game features an Amiga-style CRT scanline aesthetic, Web Audio API synthesis, single-player AI opponents, and peer-to-peer online multiplayer.

Note for Reviewers:
Engineered as a zero-dependency, single-file HTML5 application (`amiga-match3-frogger.html`), this project demonstrates client-side Web Audio synthesis, pixel-perfect Canvas rendering with continuous interpolation, state-driven AI pathfinding, and direct WebRTC (PeerJS) peer-to-peer networking.

✨ Features

🎨 Match-3 Energy & Tactical Board

- **Directional Resource Harvesting:** Match Up (▲), Down (▼), Left (◄), and Right (►) tiles to build up movement charges on your D-Pad.
- **Combo Chains & Multipliers:** Cascading matches yield double resource payouts to empower rapid movement across the field.
- **Strategic Powerups:**
  - ❄️ **Time Stop:** Freezes the world tick for 5 seconds with an icy overlay.
  - 🚩 **Checkpoint:** Establishes a permanent respawn line on the current grass row.
  - ⚡ **Boost:** Instantly grants +2 energy to all four movement directions.
  - 💥 **Destroyer:** Temporarily opens both puzzle boards to targeted block destruction.

🕹️ Amiga Canvas & Arcade Engine

- **16-Bit CRT Visuals:** Retro Amiga color palette, CRT scanline overlay, particle explosions, and screen-shake feedback.
- **Web Audio API Synthesizer:** Pure procedural sound generation (jumps, car hits, water splashes, fanfares) without external audio files.
- **Continuous Vehicle Collision:** Dual-layer collision engine using discrete tick logic combined with continuous frame-by-frame pixel interpolation.

🌐 Singleplayer AI & PeerJS Multiplayer

- **State-Driven AI Opponent:** Play against an AI featuring forward-looking path safety validation on *Easy* or *Hard* difficulty.
- **Serverless PeerJS P2P:** Real-time online 1v1 multiplayer via WebRTC data channels with authoritative host-state broadcasting and client-side move prediction.
- **Local Leaderboard:** Automatically tracks and saves the Top 5 fastest frog runs using browser `localStorage`.

🧱 Architecture & Engineering

- **Single-File Portability:** Everything (HTML, CSS, Web Audio, Canvas renderer, P2P network layer) is encapsulated inside a single file with zero build tools required.
- **Interpolated World Loop:** Decoupled 2-second world ticks with frame-rate independent visual smoothing for smooth movement.
- **Zero-Dependency Core:** Pure Vanilla JavaScript (ES6+), HTML5 Canvas, and CSS3.

📂 File Formats Supported

- Single-File Web Application (`.html`)

🚀 Deployment & Usage

How to move a Frog is a 100% client-side application.

Installation:
```bash
git clone [https://github.com/dtechniker/amiga-frogger.git](https://github.com/dtechniker/amiga-frogger.git)
