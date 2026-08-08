# Emoji Morph

A kid-friendly emoji rebus game — guess the word or phrase from the picture clues, climbing a personal staircase that gets harder the higher you go.

**[Play it here](https://anthonydeganijr-bot.github.io/emoji-morph/)**

## Features

- A personal staircase of rebus puzzles, not a shared daily puzzle — everyone climbs at their own pace
- One new rung unlocks per calendar day; solved rungs stay solved forever
- Difficulty ramps with height: simple compound words near the bottom, full idioms near the top
- Wrong guesses are low-stakes ("slipped back a step") — no lives, no game over
- A parent-assist hint reveals the rung's theme, not the answer
- Streak tracking with an honest display — a broken streak shows as broken, not stale
- Reaching the top starts a brand new climb through the same staircase
- Works offline as a single static HTML file with no build step or dependencies

## How it works

`RUNGS` in `index.html` is a hand-curated, difficulty-ordered array of emoji-clue/answer/theme triples. Progress is a single integer (`currentRung`) plus the date it was last advanced, both in `localStorage` — there's no daily seed to compute, since progression is personal rather than calendar-shared. A rung is available the moment there's no record of solving one *today* yet, regardless of how many days were skipped in between, so missing a week doesn't let a player catch up multiple rungs at once.

The streak/last-played-nudge logic is the same pattern used in Word Ladder and Crown Zones, adapted to key off "last rung solved" instead of "last daily puzzle won."

## Support

If you enjoy it, there's a [☕ tip jar](https://buymeacoffee.com/anthonydegani) in the game's footer.
