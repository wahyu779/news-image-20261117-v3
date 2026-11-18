# The Tuesday Globe — Tuesday 17 November 2026

A one-image newspaper front page summing up the world's news of
Tuesday 17 November 2026: three big lead stories, eight short reports,
a numbered world map, and nineteen more briefs — thirty stories across
six continents, from war and diplomacy to health, climate, markets
and sport. Contested claims are marked as claims, and every story
happened, or was first reported, on that Tuesday.

## How it runs

The finished picture is `entry.png` (1024 × 1024, under 1 MiB).
`main.ts` (Node 22, standard library only, no network) copies it
byte for byte to the output folder:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
# writes out/entry.png
```

Running it twice produces identical bytes.

## Files

- `page.html` — the front page itself: hand-written HTML, CSS and
  inline SVG illustrations. Every featured story carries its own
  realistic scene: the Kerch bridge arched over a dawn sea with a
  fallen road span, smoke and debris; the Strait of Hormuz with a
  fighter jet, a launch site and a burning tanker; the Quad summit
  table with four flags and four leaders; a medical tent with PPE
  workers for Ebola; a conference hall for COP31; a hospital ward
  for measles; a server room with a GPU chip for Nvidia; a
  parliament building and crowd for Serbia; a palace with
  snow-capped mountains for Mongolia; a fighter jet over the sea
  for Japan; aid trucks on a crossing road for Gaza; and a world
  map with recognisable coastlines, shaded land, labelled seas and
  twelve numbered pins.
- `entry.png` — the rendered front page, produced from `page.html`
  with headless Chromium at 1024 × 1024.
- `main.ts` — the entry program: copies `entry.png` to
  `$MAKEFUN_OUTPUT_DIR/entry.png` (or `/output/entry.png`).
- `LICENSE` — MIT.
