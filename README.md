# Wallpapers-
# HELLDIVERS 2 // Galactic War & Stratagem Terminal

A single-file, Helldivers 2 themed dashboard that runs entirely in the browser. It combines a live clock, galactic war telemetry, a stratagem codex, a stratagem-input speed game ("Hero Blitz"), daily personal orders, and a fleet leaderboard. It also works as a live wallpaper.

Everything lives in one file, `INDEX.html`. Fonts, styles, and scripts are embedded, so there is nothing to install or build.

## Features

### Super Destroyer Bridge Chronometer
- Large digital clock with a seconds sweep bar and the current date
- Toggle between 24-hour and 12-hour formats
- Galactic War day counter and a countdown to the daily reset (00:00)

### Galactic War Telemetry
- Live campaign fronts and Major Order data pulled from public Helldivers 2 community APIs
- Active Helldivers count, planet status, and Major Order briefing and timer
- Refresh button to re-sync on demand

### Stratagem Codex
- Searchable, filterable list of 100 stratagems
- Categories: Mission, Orbital, Eagle, Weapons, Packs/Mechs, Defense
- Click any stratagem to practice its directional code as an unranked drill

### Hero Blitz
A timed stratagem-input game.
- Enter the displayed code with **Arrow keys** or **W / A / S / D**
- Each successful deployment adds time back to the clock, but the time limit shrinks as your streak grows
- Score is based on code length, speed, streak, and permanent bonuses
- Best streak and best score are saved locally
- Practice drills are unranked and award 0 points

### Unlockable Themes
| Streak | Theme |
|--------|-------|
| 0 (default) | SE-GOLD |
| 5 | SE-BLU |
| 10 | BOT-RED |
| 20 | BUG-AMB |
| 30 | SQD-CYN |

Completing 10 Daily Orders permanently unlocks all five themes.

### Personal Orders (Daily Directives)
A built-in to-do list that resets daily. Completing orders earns permanent commendations:

| Orders completed | Reward |
|------------------|--------|
| 1 | Permanent +50 Blitz score bonus |
| 3 | Veteran Cape fleet crest |
| 5 | 4th Super Destroyer escort |
| 10 | All five faction themes unlocked |

### Fleet Leaderboard
- Set your own callsign and submit your best run
- Shows a global top 10 when the online leaderboard is reachable
- Falls back to a local fleet record when offline

### Now Playing Readout
- Automatically picks up track info from Lively Wallpaper, Wallpaper Engine, or the browser's MediaSession
- Can also be set manually via the edit button

### Other
- Animated orbital battlefield canvas background with tactical grid, scanlines, and vignette
- Seasonal and holiday themed events that appear automatically on the relevant dates
- Synthesized sound effects (Web Audio API) with an on/off toggle
- Hide HUD mode for a clean wallpaper view

## Usage

1. Download `INDEX.html`.
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari).
3. Start playing. Use the arrow keys or WASD to enter stratagem codes.

### Controls

| Input | Action |
|-------|--------|
| Arrow keys / W A S D | Enter stratagem direction |
| H | Hide or show the HUD |

### As a Live Wallpaper

**Lively Wallpaper**
1. Open Lively and choose **Add Wallpaper**.
2. Select `INDEX.html`.
3. Press **H** (or use the Hide HUD button) to toggle the HUD.

**Wallpaper Engine**
1. Create a new wallpaper from a web page and point it at `INDEX.html`.

The Now Playing readout syncs automatically in both.

## Data and Storage

Progress is stored in your browser's `localStorage`:

| Key | Purpose |
|-----|---------|
| `hd2_best_streak` | Best streak |
| `hd2_best_score` | Best Blitz score |
| `hd2_callsign` | Your callsign |
| `hd2_personal_orders` | Daily directives |
| `hd2_perm_medals` | Permanent medals |
| `hd2_total_orders_ever` | Lifetime completed orders |
| `hd2_last_reset_date` | Last daily reset date |
| `hd2_rewarded_today` | Orders already rewarded today |
| `hd2_manual_media` | Manual Now Playing text |

Clearing site data resets your progress.

## Network Requests

The page works offline for everything except live data. When online, it contacts:

- Helldivers 2 community APIs for campaign and Major Order data
- An online leaderboard service for the global top 10 and score submission

If any of these are unreachable, the page falls back to local or cached behavior.

## Tech Stack

- Plain HTML, CSS, and JavaScript in a single file
- Tailwind CSS (pre-compiled and inlined)
- HTML5 Canvas for the animated background
- Web Audio API for sound effects
- Embedded fonts: Inter, Orbitron, Rajdhani, Share Tech Mono (SIL OFL)

## Community

Join the squad on Discord: [The Game Lobby](https://discord.gg/EFQubt6DWy)

## Disclaimer

This is an unofficial fan project and is not affiliated with or endorsed by Arrowhead Game Studios or Sony Interactive Entertainment. Helldivers is a trademark of its respective owners.

**Spread managed democracy.**
