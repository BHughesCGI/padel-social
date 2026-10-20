# Social Padel

A self-contained padel tournament manager for a work social. Open `index.html` in a browser, or serve this folder through GitHub Pages. It needs no installation, external assets, accounts or backend to run.

## Run an event

1. Enter players and courts in Setup. Choose Mexicano or Americano, shared rally points and planned rounds.
2. Start, announce the fixtures and rests, then enter either team's score and save every match.
3. Generate the next round once all current scores are confirmed. Finish after a complete round to announce winners.
4. Export a JSON backup after each round. Import validates the backup before asking to replace the current event.

One organiser controls the event on one device. Opening the same link on another phone creates separate local data; scores do not sync. Share text summaries for updates. To transfer control, import the organiser's JSON backup on the new device and stop editing on the old device.

## GitHub Pages

Publish the root of the `main` branch through Settings > Pages > Deploy from a branch. `.nojekyll` allows the HTML to be served directly. The app contains all CSS and JavaScript, with the original unbranded green-and-lime design.

Only site files belong in this repository. Keep tournament backups, score exports and other SSC documents out of the published site. Files entered through the app stay in browser storage; they are not uploaded to GitHub.

## Offline operation

Once loaded, the app works offline in the open tab. A hosted page may require a connection to reopen or refresh after browser eviction; this single file has no service worker. A local copy works offline in a normal desktop browser. Phone file preview apps may not run JavaScript, so use the HTTPS link in iPhone Safari or Android Chrome.

Browser storage can be unavailable or cleared, and differs across browsers and profiles. Export JSON regularly. The optional timer uses an absolute deadline and catches up after screen lock, without submitting scores or guaranteeing an alarm in the background.

## Rotation and scoring

The match total is shared between teams: with 16 points, 10-6 and 8-8 are valid. Both partners receive their team's points. Rests do not invent points.

Mexicano follows neighbouring ranks after a random first round. Americano searches for varied partners and opponents. Both balance appearances and rests; neither guarantees a perfect schedule for every combination. Actual repeats are reported each round. Equal appearances rank by total points, difference and wins; unequal appearances rank by per-match points, per-match difference and win percentage. Genuine ties share positions.

Limits: 4-64 players, 1-16 courts, 1-100 shared points per match and up to 100 rounds.

## Verification

The unbranded app passed 17 engine checks and 20 browser checks, including the requested 8/2, 12/2, 10/3 and 5/1 player/court scenarios, rests, scoring, standings, refresh recovery, backups and later-round corrections. Responsive checks covered 320-1280px. Automated browser testing used Chromium; physical iPhone and Android hardware were not available.
