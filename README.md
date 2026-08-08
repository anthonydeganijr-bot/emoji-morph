# Emoji Morph

A kid-friendly emoji rebus game — guess the word or phrase from the picture clues, climbing a staircase that gets harder the higher you go. Personal, not a shared daily puzzle: everyone climbs their own pace, and there's no limit on how many rungs you solve in one sitting.

**[Play it here](https://anthonydeganijr-bot.github.io/emoji-morph/)**

## Features

- A fresh 24-rung staircase every day — climb as many rungs as you want in one sitting, no waiting between them
- Difficulty ramps with height: simple compound words near the bottom, full idioms near the top
- Wrong guesses are low-stakes ("slipped back a step") — no lives, no game over
- A parent-assist hint reveals the rung's theme, not the answer
- Streak tracking with an honest display — a broken streak shows as broken, not stale; keyed off finishing the whole day's climb, not partial progress
- Works offline as a single static HTML file with no build step or dependencies

## How it works

`RUNGS` in `index.html` is a hand-curated, difficulty-ordered array of emoji-clue/answer/theme triples, reused every day (24 rungs is exactly one day's climb). Today's progress (`rungIndex`, cumulative mistakes) lives in `localStorage` alongside the date it applies to — the moment that date isn't today, progress resets to a fresh climb. There's no daily seed to compute since the content itself doesn't change day to day, only the reset does.

The streak/last-played-nudge logic is the same pattern used in Word Ladder and Crown Zones, keyed off "finished today's full climb" instead of "solved today's daily puzzle."

## Support

If you enjoy it, there's a [☕ tip jar](https://buymeacoffee.com/anthonydegani) in the game's footer.
