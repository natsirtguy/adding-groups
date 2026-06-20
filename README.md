# Adding Groups

A self-contained, offline flashcard game that helps young kids learn single-digit
addition and subtraction. For addition, two groups of cubes slide together; for
subtraction, a group of cubes appears and some fade away when the child taps
"Take some away." Either way the child taps the answer on an on-screen keypad,
and a correct answer earns confetti and a little cheer. Subtraction always uses
the same number pairs as addition, ordered so the answer is never negative.

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

1. Cubes appear with an addition or subtraction equation — two groups to combine,
   or one group with some cubes to take away.
2. The child brings the groups together (or takes some away), counts the cubes,
   and taps the answer on the keypad.
3. A correct answer celebrates with confetti; then a new problem appears.

Designed for touch: large tap targets, no scrolling, no menus to get lost in.

## Customizing

Everything — layout, colors, and the problem logic — lives in `index.html`.
The color palette is defined as CSS variables at the top of the `<style>` block
(`--bg`, `--ink`, `--cube`, `--dot`, `--accent`), so retheming is a one-line change.

## Hosting on GitHub Pages

This repo is set up to deploy to GitHub Pages automatically. The
`.github/workflows/deploy.yml` workflow publishes the repo root (served via
`index.html`) on every push to `main`; `.nojekyll` tells Pages to serve the files
as-is without running Jekyll.

To turn it on, once the repo is on GitHub:

1. Go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **GitHub Actions**.
3. Push to `main` (or re-run the workflow) — the site builds and the live URL
   appears in the workflow's deploy step and on the Pages settings screen.

The published URL will be `https://<user>.github.io/<repo>/`.

## License

[MIT](LICENSE) — free to use, modify, and share.
