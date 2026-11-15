# Crossle

A two-word Wordle spin-off for phone browsers. Each round has a 5-letter word **across** and a 5-letter word **down** that share one letter — and the crossing point moves every round.

## How to play
- Fill all 9 squares and press Enter. Each word is scored on its own, Wordle-style (green = right spot, yellow = elsewhere in that word, gray = not in that word).
- The shared square can split diagonally: top-left half is its score in the across word, bottom-right half in the down word. Keyboard keys split the same way (top = across, bottom = down).
- Solve a word and it locks in green. 6 tries per round, 20 rounds.
- Guesses must be real words (dictionary loaded at runtime from the `an-array-of-english-words` npm package via jsDelivr; if it can't load, any letters are accepted).

## Sharing
After each round, **Share result** gives a spoiler-free emoji grid (one line per try: ➡️ across, ⬇️ down). The ☰ menu has **Share all rounds**. On phones it opens the share sheet; elsewhere it copies to the clipboard. The link in shared results is `SHARE_URL` in `index.html` (set to the GitHub Pages address).

## Run it
Open `index.html` in a browser — it's a single self-contained file. Works with GitHub Pages too (Settings → Pages → deploy from `main`).

Progress (current round, guesses, letters typed but not yet submitted, and every round's result) is saved in the browser's localStorage, so closing or refreshing the page picks up right where you left off. Progress is per browser/device.
