# NEXORA GAMING
- `website/` -> host on GitHub Pages / Vercel / Netlify (index.html, admin.html)
- `backend/` -> host on a Python server (Render, Railway, VPS, bot-hosting). Do NOT put secrets in a public repo.

## Setup
1. Fill the `NEXORA_CONFIG` block at the top of `website/index.html`, `website/admin.html`, and the config in `website/firebase-messaging-sw.js`.
2. Fill `CONFIG` at the top of `backend/main.py` (or use `.env`), add `serviceAccount.json` on the server.
3. Firebase Console > Authentication > Settings > Authorized domains: add your website domain.
4. Host `backend/` (`pip install -r requirements.txt`, run `python main.py`), put its URL in `BACKEND_URL`.
## GitHub Pages
Repo Settings > Pages > Branch `main`, folder `/website` is not selectable, so either upload the *contents* of `website/` to the repo root, or use Vercel with Root Directory = `website`.
