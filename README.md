# Lean Me Down

Personal calorie, protein, training and weight tracker. Installable on your phone (PWA), works offline, and keeps all data on the device.

## Put it on GitHub Pages (about 5 minutes)

1. On github.com create a new repository, e.g. `leanme`.
   - Free accounts need it **Public** for Pages. That's fine: only the app code is public. Your weight, meals, photos and API key never leave your phone.
2. **Add file → Upload files** and drag in everything from this folder:
   `index.html`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png`. Commit.
3. Go to **Settings → Pages**. Under *Build and deployment* choose **Deploy from a branch**, then branch `main` and folder `/ (root)`. Save.
4. After a minute your app is live at `https://<your-username>.github.io/leanme/`.

## Install on your phone

- **iPhone:** open the link in **Safari**, then Share → **Add to Home Screen**. Open it from the Home Screen icon and do the setup **there**, because Safari and the installed app keep separate storage.
- **Android:** open the link in Chrome, then menu → **Install app**.

## Photo calorie estimates (optional)

1. Create a key at console.anthropic.com → API keys, and set a monthly spend limit under Billing. A few meals a day costs cents.
2. In the app go to **Settings → AI calorie estimates**, paste the key, then Save and Test.

The key is stored only on your phone. Photos go straight from the phone to Anthropic's API.

## Updating the app later

Upload the new `index.html`, then change `VERSION` in `sw.js` (e.g. `leanme-v2`) and upload that too. The installed app picks up the update the next time it opens with a connection.

## Backups

Use **Settings → Export** every week or two, and keep the file somewhere safe. Restore it with **Import**. Photos aren't included in the backup.
