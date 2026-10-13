# VALOR STRIKE

A Valorant-style 5v5 tactical FPS in a **single HTML file** (`index.html`), rendered in 3D with Three.js (loaded from a CDN).

## How to play
Open `index.html` in a desktop browser (Chrome / Edge / Firefox). An internet connection is required to load Three.js.
Click the screen to lock the mouse.

## Features
- **Online play**: find random online players with public matchmaking, or create a party and share a code with friends; human teammates play together against bots (see below).
- **3 maps** (Dustwall, Frostline, Canal) plus a Random option, each with its own layout and color theme.
- **Valorant-style lobby**: top nav (Home / Agents / Play / Career / Collection), your 5-agent party standing in 3D, a matchmaking queue with "Match Found", a favorite agent, account level & XP, saved match history, a weapon arsenal and a settings panel. Profile and settings are saved in the browser.
- **12 agents**, each with C / Q / E abilities and an X ultimate
  - Jett: Cloudburst, Updraft, Tailwind (dash), Blade Storm
  - Phoenix: Blaze, Curveball (flash), Hot Hands (fire that heals you), Run It Back
  - Sage: Barrier Orb (destructible, you can stand on it), Slow Orb, Healing Orb, Resurrection
  - Sova: Owl Drone, Shock Bolt, Recon Bolt, Hunter's Fury (pierces walls)
  - Brimstone: Stim Beacon, Incendiary, Sky Smoke, Orbital Strike
  - Reyna: Leer (nearsight), Devour (overheal), Dismiss (invulnerable), Empress
  - Omen: Shrouded Step (short teleport), Paranoia (nearsights through walls), Dark Cover, From the Shadows (long teleport)
  - Raze: Boom Bot (chases and explodes), Blast Pack, Paint Shells (cluster grenade), Showstopper (rocket)
  - Killjoy: Nanoswarm, Alarmbot (reveals and slows), Turret (shoots enemies), Lockdown (detained enemies can't shoot)
  - Cypher: Trapwire, Cyber Cage, Spycam (reveal pulses), Neural Theft (reveals every enemy)
  - Skye: Regrowth (team heal), Trailblazer (concussing tiger), Guiding Light (long flash), Seekers (hunt and nearsight)
  - Viper: Snake Bite (acid), Poison Cloud, Toxic Screen (smoke wall through walls), Viper's Pit
- **17 weapons**, each with its own 3D model and colors (Sheriff revolver, Vandal with wood furniture, Operator with big scope and bipod, Odin with a drum…) shown in your hands, on other players, as drops, and as pictures in the shop and Collection. From the Classic to the Operator and Odin, Head, body and leg damage differ, damage drops off with range, shotguns fire pellets, snipers have scopes, sprays have recoil, and moving hurts accuracy.
- **Shop and credit economy**: 200 per kill, 3000 per round win, loss bonus of 1900 / 2400 / 2900, 300 plant bonus, 9000 credit cap. Items bought this round can be sold back.
- **Spike**: 4s plant, 45s fuse with beeps that speed up, 7s defuse with a halfway checkpoint. The spike can be dropped and picked up.
- **Round flow**: buy-phase barriers, 100s rounds, pistol rounds, side swap at half, overtime (win by 2), Competitive (first to 13), Swiftplay (first to 5) and **1v1 Duel** (first to 7, vs a bot or a friend)
- **Bot AI** (4 allies + 5 enemies, 3 difficulty levels): A* pathfinding, attacking and defending sites, rotating, reaction time, using smokes, flashes, fire and ultimates, reacting to sound, planting and defusing
- Ult orbs, weapon drops and pickups, spectating allies after death, minimap spotting, kill feed, scoreboard, damage direction indicator, flash effects, red outlines on enemies
- Positional sound effects synthesized with WebAudio (gunshots, enemy footsteps, spike beeps)

## Maps
Pick the map on the PLAY tab with the ‹ › arrows (or click the map card). In a party, the host picks and everyone sees it.
- **Dustwall**: desert outpost with a long mid corridor and a courtyard.
- **Frostline**: arctic station with a central plaza, long side lanes and tunnels.
- **Canal**: compact sunset harbor with a water street through the middle and close fights.
- **Random**: a different map every match.

## 1v1 Duel
Pick **1V1 DUEL** on the PLAY tab.
- Solo, you duel one bot. In a party of two, you duel your friend: the host is on one team and the friend on the other (a bigger party can't start a 1v1).
- First to 7 rounds, no spike: a round ends when one player is eliminated. If the 75-second timer runs out, whoever has more health and shield left wins the round.
- Both players get 5000 credits every round (full buy), a 10-second buy phase, and spawn closer together than in the 5v5 modes.
- Both players may pick the same agent. Public lobbies set to 1v1 hold two players.

## Your player name
The first time you open the game it asks for your name. Change it any time by clicking your name in the top bar (or the ✎ next to your name in the PARTY panel). Teammates and other online players see this name in the lobby, party list, killfeed and over your head.

## Play online with random players (public matchmaking)
Click **FIND ONLINE PLAYERS** (on the PLAY tab or in the PARTY panel). The game looks for an open public lobby and joins the fullest one. If none is open, it opens a new public lobby that other players can find.
- A public lobby starts on its own 30 seconds after a second player joins (5 seconds once it's full), or the host can press START.
- Agent select has a 40-second timer; anyone who hasn't locked in gets a free agent automatically.
- The host can remove a player with the ✕ next to their name.
- There are 12 public lobby slots (PUB01–PUB12). Only players running this same game can find them.

## Play online with friends (party)
1. One player clicks **PARTY** (top right of the lobby) → **CREATE PARTY** and shares the 5-letter code.
2. Friends open the same `index.html`, click **PARTY**, type the code and press **JOIN** (up to 5 players). Party chat is in the same panel.
3. The host picks the mode and bot difficulty and presses **START**. Everyone goes to agent select together; an agent locked by a teammate can't be picked again. The match starts when the whole party has locked in.

How it works:
- The whole party plays on one team against a bot enemy team; bots fill any empty slots on your team.
- The host's browser runs the match (bots, rounds, economy, spike). Each player moves and aims locally, so movement feels instant; shots, abilities and purchases are sent to the host.
- If a friend disconnects mid-match, a bot takes over their agent. If the host leaves, the party ends.
- Connections are peer-to-peer (WebRTC) using the free public PeerJS signaling server, so no account or server of your own is needed. Some strict networks (school/office Wi-Fi, some mobile carriers) can block direct connections between players.
- Testing with two tabs works — the match keeps running even when the host's tab is in the background. Both tabs share the saved profile, so give the second tab a different name.
- To test on one PC without internet, serve the folder with any local web server and open `index.html?local` in two tabs.

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
