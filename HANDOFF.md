# HANDOFF — Backwards Talk

Last updated: 15 Nov 2026. Scope: the Backwards Talk party game in `C:\dev\backwards-talk` — not any Agency/Frontstudio work.

## Goal
A reverse-audio party game Yusuf plays with family on his phone, hosted free on GitHub Pages. Done = it plays well on
his phone; further changes are whatever he asks for next.

## Current state
- **Complete:** the game is live and working. On top of Yusuf's original file: Solo mode, up to 8 teams, a New card
  button, slow-mo reverse, Family & Home and Long Phrases categories, game saved across reloads, screen kept awake, and
  four labelled replay clips on the result screen. Yusuf has played it on his Android phone (Chrome).
- **Not started:** nothing outstanding. Yusuf said "some are a bit odd" about certain cards but didn't say which ones.
- **External side effects this phase:** created the public repo `ysidat59-star/backwards-talk`, enabled Pages
  (main, root, status "built"), and pushed every commit up to `0b4c128`, plus the README/HANDOFF commit.

## Active files
| Path | Why the next session needs it | Status |
|---|---|---|
| `index.html` | the entire game; cards are in `BANK` near the top of the script | live |
| `README.md` | what it is, how to publish, features, decisions | current |

## Decisions
- Folder stays `C:\dev\backwards-talk` (Yusuf chose this over renaming it, 15 Nov 2026). Lives in `README.md`.
- One file, no framework, GitHub Pages from `main`. Lives in `README.md`.

## Dead ends and open risks
- **Unresolved:** a new category is off for anyone with a saved game, because `load()` restores the saved category list.
  To fix it, switch new categories on by default.
- **Unresolved:** recording has only been tested headless with a fake mic, plus Yusuf's own play on Android Chrome.
  It hasn't been tested on an iPhone.

## Next steps
1. Ask Yusuf what he wants changed. If it's cards, ask which ones are odd and edit `BANK` in `index.html`.
2. After any change: check the script syntax, then commit and push to `main`. Wait for the Pages build (`gh api
   repos/ysidat59-star/backwards-talk/pages/builds/latest`) and confirm the live URL serves it before saying it's live.
