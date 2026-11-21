# Junior Boy Basketball Tournament

Tournament site for a 12-team junior boys basketball tournament at Koinonia Academy: 4 groups of 3, round robin, with the top 2 in each group advancing to the quarterfinals.

The whole site is one file, `index.html`, with no build step and nothing to install. Open it in a browser.

## What it does

- **Schedule:** 12 group games in six 10-minute slots starting at 7:45 (8-minute games plus 2 minutes of warmup). Two games run at once, on Side A (left) and Side B (right).
- **Group standings:** wins, losses, points scored, points allowed and point differential. Ties are broken by head-to-head, then point differential, then points scored.
- **Knockout bracket:** quarterfinals, semifinals and championship, filled in automatically from the group results.
- **Game mode:** a full-screen scoreboard for each pair of games, with an 8:00 clock per game, a buzzer, +1 / +2 / −1 scoring and a Sync clocks button.
- **Gym info:** restrooms down the hallway, pizza and concessions at the front.

This copy includes the results from the tournament (champion: jelly fan, 19–14 over pirate token).

## Hosting on GitHub Pages

In the repo, go to **Settings → Pages**, set the source to **Deploy from a branch**, and choose `main` and `/ (root)`. The site will be at `https://<your-username>.github.io/<repo-name>/`.

## Saving scores

The original version runs as a Claude artifact, which saves results back into the page so everyone with the link sees them.

This GitHub copy can't do that. Here, scores and team names you enter are saved only in the browser you type them in, and other people won't see them. To share new results, edit the `tourney-state` data in `index.html` (search for `tourney-state`) and commit it, or keep using the Claude version for live tournaments.

To reuse the site for a new tournament, replace the `tourney-state` line with:

```html
<script type="application/json" id="tourney-state">{"v":1,"rev":0,"teams":{},"games":{},"ko":{}}</script>
```
