# Workout — Unlock & Build

Personal workout app: **https://dlhackbart.github.io/workout/** (single file, `index.html`; works on phone, laptop, TV).

## The plan (v2, 2026-09-25)
Built to undo years of sitting — movement, flexibility and back strength first; cardio later.
Two routines, **alternated daily** (the app counts from 2026-09-25 = A; miss a day → just tap the other tab):

| Tab | What | Time |
|---|---|---|
| **A · Unlock** | 10 mobility moves (hips, spine, hamstrings, chest, posture) + balance finish | ~30 min |
| **B · Build** | 10 back-first strength moves (McGill Big 3, bridges, rows, hinge, squat, push-up) + balance finish | ~30–35 min |
| **Desk Reset** | 4 moves, 2 min, every hour of sitting | 2 min |

**Balance finish** (end of both routines): feet-together stand, heel-to-toe stand, single-leg stand, heel-to-toe walk — always at a counter.
Full exercise list, doses and video links: [`workout_plan.md`](workout_plan.md).

## Using the app
- **Tap an exercise** to check it off; the voice announces the next one.
- **Tap the thumbnail** → the demo video plays full-screen and loops while you do your sets; **✓ Done — next** checks it off.
- **📺 Auto-video** opens the next exercise's video automatically.
- **Sets / weight** boxes log actuals vs plan; **📊 Stats** shows streak and 14-day history. Data lives in the browser's localStorage (per device).

## Sending videos to the TV (Roku / smart TV / Chromecast)
Same Wi-Fi; YouTube app installed on the TV.
- **Per exercise (recommended):** on the phone, tap a thumbnail → **📺 Play on TV** → opens the YouTube app → tap **Cast** → pick the TV. While the YouTube app stays connected, every later "Play on TV" goes straight to the TV.
- **Whole routine:** **📺 Whole routine → TV** opens every video of the current tab as one YouTube playlist; cast it once. Videos are ~1 min, so pause between exercises.
- **Mirror the laptop:** Win + K → pick the Roku (enable Settings → System → Screen mirroring on the Roku).

## Videos
Every video id was checked 2026-09-25 for title, channel, length and **embeddability** (`yt-dlp … %(playable_in_embed)s`) — mostly physical-therapy clinic channels. Not every video was watched end to end; swap any that demonstrate poorly by changing its `v:` id in `index.html` (and the link in `workout_plan.md`).
YouTube embeds can fail when the page is opened as a local `file://` — use the GitHub Pages URL.

## Files
- `index.html` — the app (the plan lives in the `PLAN` / `BALANCE` constants at the top of the script)
- `workout_plan.md` — printable plan with video links
- `weight_log.md` — manual weight log
- `clips/` — v1 still-frame clips (unused since v2; kept)

## History
- **v2 — 2026-09-25:** replaced the 7-day strength plan with A/B Unlock & Build + Desk Reset, embedded PT demo videos, TV casting buttons, balance finish on both routines. Storage keys moved to `wk2_*` (v1 history is untouched under `wk_*`).
- **v1 — 2026-06-26:** 7-day strength & mobility plan with still-frame clips. Local archive: `Downloads\_swplan\workout_v1_2026-06-26.html` and `workout_plan_v1_2026-06-26.md`; also in this repo's git history.
