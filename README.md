# Squeekchain Wheel Prediction Game

Predict whether the next Squeekchain block completes within 60 seconds — settled by the chain's own live readings. Free to play, no wallet, no transactions.

## How it works

- The page reads Squeekchain's public API (`https://api.squeekchain.com/v1/status`) live: hamster state, RPM, block height and block progress.
- You call YES or NO on whether the next block completes within 60 seconds, with toy "seeds" (10 / 25 / 50). A correct call pays back double your bet.
- Settlement uses two live reads (block height at lock-in vs after the deadline) on the local clock. If the feed cannot confirm a round, the bet is voided and refunded.
- The wheel animation follows the hamster's real RPM; when he sleeps, the wheel is idle and blocks take far longer than 60 seconds.

## Play it

Live site: _(add your domain / GitHub Pages URL here once deployed)_

Just open `index.html` in a browser — no build step, no server needed.

## Deploy (GitHub Pages, free)

1. Create a public GitHub repository for this project.
2. Upload `index.html` and this `README.md` to the repository.
3. In the repository: Settings → Pages → Source: Deploy from a branch → Branch: `main`, Folder: `/ (root)` → Save.
4. The game is live at `https://<username>.github.io/<repo>/`.

## Squeekchain Genesis verification

> Paste the three verification items from your Genesis profile here once you start the direct submission at https://squeekchain.com/genesis/code — do not invent them.

- **DNS record:** _(paste the record Squeekchain gives you; add it to your domain's DNS)_
- **Page tag:** _(paste the tag Squeekchain gives you; it goes in the live site's HTML)_
- **Repository line:** _(paste the line Squeekchain gives you; it goes in this README)_

After all three are in place, press Verify in your Genesis profile. The Squeekchain team reviews the project, then it appears on the Genesis board.

## Notes

- Static site, session-only score (refresh resets the burrow).
- The game is distinct from Spoke Sprint (20s race), Squeek Out (bail timing) and Squeek or Sleep (nap/jog/zoomies): it is a 60-second block-completion prediction settled on live readings.
