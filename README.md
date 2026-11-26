# The Night Hotel / 永夜旅馆

A first-person horror stealth game built with **Three.js**, made for the Week 05 3D browser
game assignment and republished for Week 07. You are the night manager: restore the hotel's
power, use the cameras and the phone, and get back to the security room alive.

**Play in your browser:** <https://luze-111.github.io/pac-man/>

> **Content warning.** Jump scares, horror imagery, sudden loud audio and rapid camera
> movement. Start with the volume low. Press `Esc` to pause or leave at any time.

## What you do

The hotel is dark and the power is out. Find the distribution boxes, hold `E` to repair them,
avoid *The Last Guest*, and return to the security room. Close the security-room door behind
you to finish the night. Cameras, room phones and the bed hiding spot are your tools. This
build covers Night 1.

## Controls

| Action | Key |
| --- | --- |
| Move / look | `WASD` / mouse |
| Run (audible footsteps) | `Shift` |
| Quick turn | middle mouse button |
| Interact / hold to repair | `E` |
| Phone (map, apps, cameras) | `Space` to stow or raise |
| Full-screen cameras | `M` |
| Night vision (90 s battery) | `Q` |
| Phone flashlight | `F` |
| Ring room 201 / 202 | `1` / `2` |
| Use held item | `V` |
| Pause | `Esc` |

## Run locally

Requires **Node.js 18+** and a desktop browser with WebGL2. Nothing needs to be installed:
Three.js and all assets are vendored in the repository.

```sh
git clone https://github.com/luze-111/pac-man.git
cd pac-man/w05_3d_game
node server.mjs
```

Open <http://127.0.0.1:5182/>. On Windows you can also double-click `START_GAME.cmd`.
Do not open `index.html` directly — ES modules need an HTTP server.

Run the tests with:

```sh
cd w05_3d_game
node --test tests/*.test.mjs
```

## Repository layout

```text
README.md                 this file
w05_3d_game/
  index.html              game entry
  server.mjs              dependency-free static server
  src/                    gameplay, rendering, audio, UI
  assets/                 textures, audio, fonts, maps
  vendor/                 Three.js r180 (local copy)
  tests/                  node:test suites
```

## Known limits

- Desktop keyboard and mouse only; there are no touch controls.
- Needs WebGL2; older integrated GPUs may run slowly.
- Progress is not saved across a page reload.
- Static hosting only — there is no backend or online multiplayer.
- `github.io` is not reachable from mainland China without a proxy.

## Credits and licences

- **Three.js r180** — MIT licence, vendored in `w05_3d_game/vendor/`.
- **VT323 font** — SIL Open Font License, see `w05_3d_game/assets/fonts/vt323/OFL.txt`.
- **Heartbeat recording** — InspectorJ, CC BY 4.0; see `w05_3d_game/assets/audio/heartbeat/README.md`.
- **Enemy and tutorial audio** — sources listed in `w05_3d_game/assets/audio/enemy/README.md`
  and `w05_3d_game/assets/audio/tutorial/README.md`.
- **Materials, music and voice** — ambientCG textures (Lennart Demes, CC0), AI-generated
  textures, music by Chris Pinkston, and the AI supervisor voice are listed with their terms
  in `w05_3d_game/REFERENCE_NOTES.md`; third-party assets keep their original licences.
- **Visual reference** — the character design refers to MOMO; interface and pacing refer to
  *Five Nights at Freddy's* and *Dark Deception*. Models and scenes are our own work.
  Full list: `w05_3d_game/REFERENCE_NOTES.md`.
- **AI assistance** — scope recorded in `w05_3d_game/AI_ASSISTANCE.md`. Documentation and
  deployment for Week 07 were prepared with DeepSeek Harness at the team's request.

## Contributors

Everyone confirms their own row. Publishing does not make one person the sole author.

| Name | GitHub | Contribution |
| --- | --- | --- |
| 卢泽 (Lu Ze) | [@luze-111](https://github.com/luze-111) | Publisher: repository, README, GitHub Pages deployment |
| — | [@MaybeItsAI](https://github.com/MaybeItsAI) | Documentation — to confirm in own PR |
| 冯宏远 (Feng Hongyuan) | [@Fhy11401](https://github.com/Fhy11401) | Documentation: Credits section — asset, music and voice licences |
| — | [@Mikuuuuuchan](https://github.com/Mikuuuuuchan) | Documentation — to confirm in own PR |

**How to update this table:** each member edits only their own row, in their own branch and
pull request, replacing the placeholder with their registered name and a one-line summary of
the work they actually did. Do not edit another member's row.
