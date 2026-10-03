# Brick Coffee

A private log of the specialty coffee I buy and the shots I pull from it.

Register a bag once (roaster, origin, process, roast level, roast date, target
time). Then every brew is four numbers — dose in, grind setting, yield out,
seconds — captured with big steppers you can hit one-handed. When you save, the
app says whether to go finer, go coarser, or hold, and suggests the actual grind
number to try next time.

It works out which direction your grinder's numbers run by watching your own
shots: after three or four brews at different settings, "go finer" becomes
"try 4.6".

## Running it

It's a static site — no build step, no dependencies.

```
python3 -m http.server 8777
```

Then open http://localhost:8777

## On your phone

Open the published URL in Chrome, then **⋮ → Add to home screen**. It opens full
screen with its own icon, works with no signal, and updates itself whenever you
open it online — nothing to reinstall.

## Your data

Everything is stored in the browser's localStorage on that one phone. It is never
uploaded anywhere. **Backup & data → Export a backup file** writes a JSON file you
can keep; restoring it on a new phone brings the whole log across.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The entire app — markup, styles, logic and the two embedded fonts |
| `sw.js` | Service worker: offline cache, network-first on navigation so updates land |
| `manifest.webmanifest` | Makes it installable as an app |
| `icon-*.png` | Generated two-ink icons |
