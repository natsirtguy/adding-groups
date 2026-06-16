# Adding Groups

A self-contained, offline flashcard game that helps young kids learn single-digit
addition. Two groups of cubes slide together, the child taps the total on an
on-screen keypad, and a correct answer earns confetti and a little cheer.

There is nothing to install or build — it's a single static HTML file with no
dependencies, no network calls, and no tracking.

## Play it

Open `index.html` in any modern browser (desktop or mobile). That's it.

Or host it anywhere that serves static files — because the entry point is
`index.html`, it works as-is on GitHub Pages, Netlify, or any static host:

```bash
# quick local server (optional — opening the file directly also works)
python3 -m http.server 8000
# then visit http://localhost:8000
```

## How to play

1. Two groups of cubes appear with an addition equation.
2. The child counts the cubes and taps the answer on the keypad.
3. A correct answer celebrates with confetti; then a new problem appears.

Designed for touch: large tap targets, no scrolling, no menus to get lost in.

## Customizing

Everything — layout, colors, and the problem logic — lives in `index.html`.
The color palette is defined as CSS variables at the top of the `<style>` block
(`--bg`, `--ink`, `--cube`, `--dot`, `--accent`), so retheming is a one-line change.

## License

Free to use and share. Add a `LICENSE` file (e.g. MIT) if you publish it.
