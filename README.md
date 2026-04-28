[README.md](https://github.com/user-attachments/files/27150667/README.md)
# BULLY SAID — Anime Opening (Fragman)

A browser-based animated anime opening for the fictional shonen series **"BULLY SAID"** — built as a single self-contained HTML file. 2 minutes of timed scenes, original synth-rock score generated live with the Web Audio API, and two interactive tap-mini-games that unlock at the end.

## ✨ Features

- **8-scene timed opening** (2:00 runtime) — studio card → title drop → 3 character intros → 2 action scenes → final teaser
- **3 SVG character portraits** with hometown badges and stat blocks
  - SAID — the bully · Istanbul · brunette · muscular
  - OMER OSMAN — victim one · Eskişehir · buzzcut · skinny
  - MEFO — victim two · Kayseri · blonde · skinny
- **Original synth-rock soundtrack** generated at runtime with the Web Audio API (no audio files, no copyright issues). 120 BPM, E-minor pentatonic lead over a 4-bar progression, drums + bass + lead.
- **Two interactive tap-games** that auto-open after the intro:
  - **GAME 01 — PUNT MEFO** — tap-to-kick whack-a-mole, 15s
  - **GAME 02 — HOLD OMER** — grip-strength holdout, 15s
- **HUD controls** — replay, mute toggle, skip-to-games
- **No dependencies** — pure HTML/CSS/JS/SVG. Just open `index.html` in any modern browser.

## 🚀 Quick Start

### Option 1 — Open locally
```bash
git clone https://github.com/YOUR_USERNAME/bully-said-anime.git
cd bully-said-anime
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

### Option 2 — Deploy to GitHub Pages
1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, select branch `main` and folder `/ (root)`.
4. Save. Your opening will be live at `https://YOUR_USERNAME.github.io/bully-said-anime/`.

That's it — no build step, no bundler, no npm install.

## 🎬 Scene Breakdown

| # | Scene | Time | Description |
|---|---|---|---|
| 1 | Studio Card | 0:00 – 0:08 | "Said-Obi Studios" production logo |
| 2 | Title Drop | 0:08 – 0:20 | Smashing title slash effect |
| 3 | Character · SAID | 0:20 – 0:42 | Bully reveal, red palette |
| 4 | Character · OMER OSMAN | 0:42 – 1:02 | Victim one, teal palette |
| 5 | Character · MEFO | 1:02 – 1:22 | Victim two, gold palette |
| 6 | Action — DANGLE!! | 1:22 – 1:40 | Said dangling Omer from a school window |
| 7 | Action — PUNT!! | 1:40 – 1:54 | Said punting Mefo across the hallway |
| 8 | Coming Soon | 1:54 – 2:00 | Final title card |

## 🎮 Mini-Games

### Game 01 — PUNT MEFO
Mefo appears at a random spot on screen. Tap him to send him flying off-screen with a "PUNT!" SFX. Each tap = 1 point. 15-second round.

### Game 02 — HOLD OMER
Said leans out the window holding Omer by the ankle. The grip-strength bar drains over time, faster as seconds pass. Tap anywhere in the panel to tighten the grip (+8 grip, +2 score, with a wiggle).

- Survive 15 seconds → **HELD ON!** +50 bonus
- Grip hits zero → **DROPPED!** Omer falls with a descending sawtooth scream.

Both games feed into a combined score at the top of the screen.

## 🛠 Tech

- **HTML5** — single-file structure, no build step
- **CSS3** — keyframe animations, flexbox/grid layout, custom properties
- **SVG** — all character art and action scenes drawn inline
- **Vanilla JS** — scene timing via `requestAnimationFrame`, game logic, no frameworks
- **Web Audio API** — runtime synth using oscillators, biquad filters, waveshaper distortion, dynamics compressor, and a [Chris Wilson-style lookahead scheduler](https://www.html5rocks.com/en/tutorials/audio/scheduling/) for drift-free timing

### Browser support
Tested in modern Chrome, Firefox, Safari, and Edge. Requires Web Audio API support (basically anything from the last 8 years).

## 📁 Project Structure

```
bully-said-anime/
├── index.html          # Everything — scenes, audio engine, games
├── README.md
├── LICENSE
└── .gitignore
```

That's the whole repo. One file, no dependencies.

## 🎨 Customizing

Want to riff on this? Easy edits inside `index.html`:

- **Scene timings** — edit the `scenes` array at the top of the `<script>` block.
- **BPM / key** — change `BPM` constant and the `BASS_ROOTS` / `LEAD_PATTERN` arrays.
- **Character details** — find the `<section class="scene" id="s3">` (and s4, s5) blocks and edit the `.name`, `.hometown`, `.desc`, and `.stat` elements.
- **Colors** — tweak the `:root` CSS custom properties (`--blood`, `--gold`, `--teal`, etc.)
- **Game difficulty** — adjust `g2Grip` drain rate or game duration in `startGame1` / `startGame2`.

## ⚠️ Notes

- The audio is an **original synth placeholder**. It is not copyrighted music. If you want to use a real track, mute the synth (🔇 button) and play your own audio externally.
- All violence is cartoony / Looney Tunes-style slapstick. No graphic content.
- Names and characters are fictional.

## 📄 License

MIT — see [LICENSE](./LICENSE).

## 🙌 Credits

- Built with Claude (Anthropic).
- Fonts via Google Fonts: *Bebas Neue*, *Bungee Inline*, *Noto Serif JP*, *Special Elite*, *Zen Dots*.
- Inspired by classic shonen anime openings — direction, not direct quotation.
