# FlipLingo

Interactive two-language flashcards in a single HTML file. No install, no build, no server.

## Use it

- **Online:** open the GitHub Pages site for this repository.
- **Offline:** download `index.html` and open it in your browser by double-clicking it. An internet connection is needed on first load to fetch React and Babel from a CDN.

## How it works

1. **Setup** — name your two languages (defaults: Français and Nederlands), pick the test direction, and choose whether to shuffle.
2. **Edit cards** — paste your deck, one card per line (format below). **⇄ Swap columns** flips front and back on every line if you pasted them in the wrong order.
3. **Practice** — tap a card to flip it, then mark it Correct or Incorrect.
4. **Results** — see your score and the cards you missed; retry just the mistakes, restart the full set, or go back to setup.

Nothing is saved: decks and results live in memory, and reloading the page restores the sample deck. Keep your decks as text files.

## Deck format

Plain text, one card per line, front and back separated by `|`. Whitespace around each side is trimmed; lines without a `|` or with an empty side are ignored.

```
maison | huis
livre | boek
je viens (venir) | ik kom (komen)
```

The first column is Language A (front), the second is Language B (back).

## Development

Everything lives in `index.html`: React 18 and Babel standalone load from cdnjs, and the JSX in the page is compiled in the browser. Edit the file and reload. It must keep working when opened directly from disk, so there is no build step.

## License

[MIT](LICENSE)
