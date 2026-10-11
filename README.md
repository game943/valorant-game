# VALOR STRIKE

A Valorant-style 5v5 tactical FPS in a **single HTML file** (`index.html`), rendered in 3D with Three.js (loaded from a CDN).

## How to play
Open `index.html` in a desktop browser (Chrome / Edge / Firefox). An internet connection is required to load Three.js.
Click the screen to lock the mouse.

## Features
- **Valorant-style lobby**: top nav (Home / Agents / Play / Career / Collection), your 5-agent party standing in 3D, a matchmaking queue with "Match Found", a favorite agent, account level & XP, saved match history, a weapon arsenal and a settings panel. Profile and settings are saved in the browser.
- **6 agents**, each with C / Q / E abilities and an X ultimate
  - Jett: Cloudburst, Updraft, Tailwind (dash), Blade Storm
  - Phoenix: Blaze, Curveball (flash), Hot Hands (fire that heals you), Run It Back
  - Sage: Barrier Orb (destructible, you can stand on it), Slow Orb, Healing Orb, Resurrection
  - Sova: Owl Drone, Shock Bolt, Recon Bolt, Hunter's Fury (pierces walls)
  - Brimstone: Stim Beacon, Incendiary, Sky Smoke, Orbital Strike
  - Reyna: Leer (nearsight), Devour (overheal), Dismiss (invulnerable), Empress
- **17 weapons**, from the Classic to the Operator and Odin. Head, body and leg damage differ, damage drops off with range, shotguns fire pellets, snipers have scopes, sprays have recoil, and moving hurts accuracy.
- **Shop and credit economy**: 200 per kill, 3000 per round win, loss bonus of 1900 / 2400 / 2900, 300 plant bonus, 9000 credit cap. Items bought this round can be sold back.
- **Spike**: 4s plant, 45s fuse with beeps that speed up, 7s defuse with a halfway checkpoint. The spike can be dropped and picked up.
- **Round flow**: buy-phase barriers, 100s rounds, pistol rounds, side swap at half, overtime (win by 2), Competitive (first to 13) and Swiftplay (first to 5)
- **Bot AI** (4 allies + 5 enemies, 3 difficulty levels): A* pathfinding, attacking and defending sites, rotating, reaction time, using smokes, flashes, fire and ultimates, reacting to sound, planting and defusing
- Ult orbs, weapon drops and pickups, spectating allies after death, minimap spotting, kill feed, scoreboard, damage direction indicator, flash effects, red outlines on enemies
- Positional sound effects synthesized with WebAudio (gunshots, enemy footsteps, spike beeps)

## Controls
| Key | Action |
|---|---|
| WASD / Shift / Ctrl / Space | Move / Walk (silent) / Crouch / Jump |
| Left click / Right click | Fire / Aim · Scope |
| R | Reload |
| 1 2 3 | Primary / Sidearm / Knife |
| C Q E X | Abilities / Ultimate |
| 4 (hold) | Plant or defuse the spike |
| F | Pick up weapon / Collect ult orb |
| G | Drop the spike |
| B | Shop (buy phase) |
| Tab | Scoreboard |
| Esc | Pause |
