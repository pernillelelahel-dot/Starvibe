# STARVIBE — GitHub Pages

This folder is the GitHub Pages-ready version of STARVIBE.

## Publish on GitHub Pages

1. Create a **public** GitHub repository.
2. Upload every file in this folder to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**.
6. Click **Save**.

Your site will normally be available at:

`https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`

## Firebase

STARVIBE still uses Firebase for FanZone chat and the administrator area.

Make sure the Firebase project has:
- Anonymous Authentication enabled (for FanZone)
- Email/Password Authentication enabled (for administrators)
- Realtime Database enabled
- Database rules configured appropriately

## Live feed

GitHub Pages cannot run the original Cloudflare Worker, so the Cloudflare `/api/feed` endpoint was removed.

The site now checks:
1. Firebase `liveFeed/items`
2. `feed.json`

`feed.json` starts empty so the site never displays fabricated news.

## Files removed from the GitHub Pages version

The Cloudflare-only files (`_worker.js`, `wrangler.jsonc`, and the original Cloudflare deployment instructions) are intentionally not included.
