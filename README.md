# News Image — Tuesday 17 November 2026

A newspaper front page that sums up the world's news of Tuesday
17 November 2026 in one image, built for make.fun's
`news-image-20261117` bounty.

## The day in four stories

- **KERCH BRIDGE HIT** — Ukraine strike collapses a road span to
  Crimea; Russia hits two Kyiv bridges in reply.
- **TRUMP LANDS IN MANILA** — ASEAN summit opens the Asia trip; trade
  pact with Thailand signed, Xi–Putin talks ahead.
- **TANKERS HIT AT HORMUZ** — Iran says mines struck two tankers;
  third US carrier reaches the Gulf.
- **EU PLANS RWANDA HUB** — Five states to send rejected asylum
  seekers to a return centre in Rwanda.

Ticker: JPMorgan blames a software bug for the bank outage; the Vulcan
rocket fails and 40 Amazon satellites are lost; Nvidia reports its
first earnings since Huang's exit; the Pentagon fails its audit for the
9th year; WHO: Eritrea ends trachoma.

## How it is built

`entry.png` is a 1024×1024 front page composed with PIL: four
AI-generated editorial illustrations (no text in them) under a masthead
and exact headlines, captions and ticker text rendered by PIL, so every
word is spelled exactly right. The file holds JPEG bytes under the name
`entry.png` — the gate reads the format from the first bytes — because
a PNG of this photo-heavy page ran over the 1 MiB gate.

`main.ts` (Node 22, standard library only) copies `entry.png` to
`/output/entry.png` byte for byte, after checking the magic bytes, the
1 MiB size cap and the 1024×1024 pixel cap from the JPEG SOF marker.
Both grading runs write the identical bytes.

Run it locally with:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

## Licence

MIT — see `LICENSE`.
