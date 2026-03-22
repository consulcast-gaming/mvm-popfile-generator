# MvM Popfile Creator

A desktop app for creating TF2 Mann vs. Machine popfiles.

## Quick Start (Browser Only)

1. Install Node.js from https://nodejs.org (LTS version)
2. Open a terminal in this folder
3. Run these commands:

```
npm install
npm run dev
```

4. Open http://localhost:5173 in your browser

## Build as Desktop App (.exe)

### Option A: Portable .exe (recommended)

```
npm install
npm run package
```

This creates a portable .exe in the `release` folder. No installation needed — just double-click to run.

### Option B: Run with Electron (no packaging)

```
npm install
npm run electron-dev
```

This builds the app and opens it in an Electron window directly.

### Option C: Static HTML (no server needed)

```
npm install
npm run build
```

Open `dist/index.html` directly in your browser. You can make a desktop shortcut to this file.

## Troubleshooting

- If `npm install` fails, try deleting `node_modules` and `package-lock.json`, then run `npm install` again
- If Electron packaging fails, make sure you're on Windows and try `npx electron-builder --win`
- The app works offline — no internet needed after building

## How to Use the .pop File

1. Export your mission using the .pop button
2. Place the file in: `tf/scripts/population/`
3. In TF2, open console and type: `map <mapname>` then `tf_mvm_popfile <filename>`

## Features

- **Settings** — Map name, starting currency, respawn time, difficulty
- **Missions** — Sentry busters, spies, snipers, engineers with cooldowns and wave ranges
- **Bot Creator** — Build custom bot templates with items, CharacterAttributes, ItemAttributes
- **Waves** — Unlimited waves with Single/Squad/RandomChoice/Tank wavespawns
- **All Valve templates** — Verified against robot_standard.pop, robot_giant.pop, robot_gatebot.pop
- **Editable previews** — Auto-generated code you can hand-edit for full control
- **Light/Dark mode**
