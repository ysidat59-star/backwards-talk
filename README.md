# Backwards Talk

A reverse-audio party game for playing on a phone with family. Personal project, not Frontstudio work.

**Live:** https://ysidat59-star.github.io/backwards-talk/
**Repo:** https://github.com/ysidat59-star/backwards-talk (public)
**Local folder:** `C:\dev\backwards-talk`

## How it's built

The whole game is one file, `index.html`: HTML, CSS and plain JavaScript, with no build step and no dependencies.
The phrase cards are in the `BANK` object near the top of the script. Audio is recorded with `MediaRecorder` and reversed
with the Web Audio API. The microphone only works over https (or from a local file), and GitHub Pages provides the https.

## Changing and publishing

1. Edit `index.html`. To try it, double-click the file to open it in Chrome.
2. Commit and push to `main`. GitHub Pages rebuilds in about a minute, and then the live link has the change.
3. On the phone, pull down to refresh.

## Features

- **Game modes:** Teams (2–8 teams) or Solo (2–8 players, each for themselves), plus Free play (record anything, hear it backwards).
- **Solo scoring:** the player who guesses first and the performer each get +1.
- **Categories:** Celebrities, Phrases, Long Phrases (50 sayings of 3–6 words), Films & TV, Food & Drink, Animals, Family & Home, Places.
- **During a round:** New card button in step 1, and a slow-mo (0.75×) option for the reversed clip.
- **Result screen:** replays all four clips, labelled 1–4: Original, Original reversed, The copy, Copy flipped back.
- **Memory:** teams, scores and settings survive a reload (stored in `localStorage`), and the screen stays awake during a game.

## Decisions

- **Hosting:** GitHub Pages from `main`, root folder. **Folder:** `C:\dev\backwards-talk`, kept rather than renamed. *(15 Nov 2026)*
- **One file, no framework.** Keep it that way unless the game outgrows it.
- **The game records only the performer.** Guessers answer out loud and are never recorded.
- **Known quirk:** a new category starts switched off for anyone with a saved game, because saved settings remember the old category list.
