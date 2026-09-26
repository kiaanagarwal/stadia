# Stadia

Every match in the world today: who's playing, which ground, and where to watch.

- Live scores for cricket, football, tennis, hockey, baseball, rugby, MMA and more, pulled from ESPN's public scoreboard feed
- Tap a match for highlight videos, the full ground name and city, and the channels showing it
- Sign-in page with email accounts

It's a single static page (`index.html`) with no build step. Open it in a browser, or deploy the folder as-is (Netlify config in `netlify.toml`).

## Sign-in

Account emails and passwords live in `login-details.txt`, which is kept out of git. The page stores only SHA-256 fingerprints of `email:password`. This is a simple gate, not real security: anyone who can read the page's code can get past it.
