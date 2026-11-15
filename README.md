# MACHI まち — a scroll-world demo

One small clay-diorama Japanese town, one whole day. Scroll, and the camera
flies through Machi in a single continuous take — morning arrival over the
town island, the shotengai shopping street, the canal at golden hour, shrine
steps at dusk, the night market, and a finale inside the glow of a giant
paper lantern.

## How it works

- 11 AI-generated video clips (6 scene dives + 5 aerial connectors, Veo 3.1
  Lite via Google Flow) chained with frame-identical seams: every connector
  was generated from the *actual* last frame of one dive and first frame of
  the next, then verified by PSNR (starts 34.6–35.9 dB, ends 21.1–32.9 dB).
- A scroll-scrub engine (`scrub-engine.js`) maps scroll position to video
  time across the whole chain — no cuts, no autoplay.
- Clips are encoded for scrubbing: 720p, crf 20, GOP 8, faststart.
- Static site, no build step: open `index.html` or serve the folder.

## Credits

Total generation cost: 120 Flow credits (12 videos × 10; all stills free).
