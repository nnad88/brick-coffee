# Cafecito

*Pequeño pero poderoso.* A private log of the specialty coffee I buy and the
shots I pull from it.

Open it and the first thing you see is your recent shots. The big **+** at the
bottom starts a new one: pick the bag, then set four numbers — dose in, grind
setting, yield out, seconds — with steppers you can hit one-handed. Dose has
**14 g** and **18 g** shortcuts because those are the two I actually use.

When you save, it tells you to go finer, go coarser, or hold, and suggests the
grind number to try next time. It works out which direction your grinder's
numbers run by watching your own shots: after three or four brews at different
settings, "go finer" becomes "try 4.6".

## Running it

A static site — no build step, no dependencies.

```
python3 -m http.server 8777
```

Then open http://localhost:8777

## On your phone

Open the published URL in Chrome, then **⋮ → Add to home screen**. It opens full
screen with its own icon, works with no signal, and updates itself whenever you
open it online — nothing to reinstall.

## Your data

Stored in the browser's localStorage on that one phone, never uploaded. There
is no export/import in the app itself, so it lives and dies with that phone's
browser storage.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app — markup, styles, logic, and three embedded fonts |
| `sw.js` | Service worker: offline cache, network-first on navigation so updates land |
| `manifest.webmanifest` | Makes it installable as an app |
| `icon-*.png` | Generated cup icons (no saucer) |
