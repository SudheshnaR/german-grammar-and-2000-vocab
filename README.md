# Hörbar

A single-file German learning app. No build step, no dependencies, no server — one HTML file that runs offline in the browser.

Built for learning German in Switzerland (Swiss spelling: `ss` rather than `ß`).

## What's in it

**Wörter** — 2,044 words and 150 phrases across 60 themed sets.

- Each entry is spoken aloud: the word, a pause, then an example sentence
- Auto-play works through a whole set hands-free
- Slow mode, repeat, and a listening-first mode that hides the English
- Phrase sets cover real situations — the council office, the doctor, a job interview, parents' evening, small talk, the phone. Each speaks your line, then a likely reply

**Grammatik** — 54 topics, 946 exercises, A1 to B1.

- Follows the standard A1–B1 grammar progression, in order
- Every topic opens with conjugation and declension tables, reachable at any time via the **Formen** button
- German grammar terms carry English glosses (Akkusativ → *direct object*)
- Fill-in-the-blank and multiple choice, checked with an explanation of *why*
- Answer checking is forgiving: case-insensitive, punctuation ignored, `groesser` accepted for `grösser`, and alternative correct answers allowed
- Progress saved per topic

## Running it

Open `index.html` in any browser. That's the whole setup.

### On an iPhone

1. Open the page in Safari
2. Share → **Add to Home Screen** — it then opens like an app, offline

For audio, a German voice must be installed:
**Settings → Accessibility → Spoken Content → Voices → German**

Audio stops when the screen locks, so keep the screen awake during auto-play.

### GitHub Pages

With this repo on GitHub: **Settings → Pages → Source: deploy from branch → main → / (root)**.
The app is then live at `https://<username>.github.io/<repo>/`.

## Technical notes

- One file, ~385 KB, no external requests
- Speech via the browser's built-in `SpeechSynthesis` API — no audio files, no network
- Progress stored in `localStorage`, wrapped so it degrades gracefully where storage is unavailable
- Prefers a `de-CH` voice, then `de-DE`, then any German voice

## Content

All vocabulary, example sentences, grammar explanations and exercises are original, written for this app. Nothing is reproduced from any textbook or published word list.

## Licence

MIT for the code. Do what you like with it.
