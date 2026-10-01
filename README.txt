STARVIBE — Cloudflare Static Upload + Firebase backend

WHAT IS INCLUDED
- index.html — full STARVIBE site
- admin.html — Firebase administrator panel
- firebase-config.js — your existing STARVIBE Firebase web config

DEPLOY TO CLOUDFLARE
1. In Cloudflare Workers & Pages choose Create application.
2. Choose Upload your static files.
3. Upload the CONTENTS of the cloudflare-site folder (or ZIP this folder and upload it if the uploader accepts ZIP).
4. Deploy.
5. Open /admin.html for the administrator panel.

FIREBASE REQUIREMENTS
- Authentication: enable Anonymous and Email/Password providers.
- Realtime Database: use the rules supplied in ../firebase-backend/database.rules.json.
- Add your administrator UID at /admins/YOUR_USER_UID = true.

LIVE FEED
The site first reads /liveFeed/items from Firebase. If that node is empty, it falls back to live RSS sources through RSS2JSON and maintains a Johnny Depp-focused mix (up to 60% of the displayed feed).

IMPORTANT
The Firebase web config is not a password/secret. Protect your database with the rules provided in the backend folder.
