# Form — Workout Planner (offline PWA)

Static files only. No build step, no server, no accounts inside the app.

```
index.html            the whole app
sw.js                 service worker (makes it work offline)
manifest.webmanifest  install info (name, icons, colors)
fonts/ icons/         self-hosted font and app icons
```

## Deploy (GitHub Pages, free, about 5 minutes)

1. Create a new GitHub repo, e.g. `form-workout`.
2. Upload everything in this folder to the repo root (keep the `fonts/` and `icons/` folders).
3. Repo > Settings > Pages > Source: Deploy from a branch > `main` / `/ (root)` > Save.
4. Wait a minute. Your app is at `https://<your-username>.github.io/form-workout/`.

Other free hosts with HTTPS also work: Netlify (drag the folder onto app.netlify.com/drop while logged in), Cloudflare Pages, Vercel. HTTPS is required for offline mode.

## Install on your phone

- Android (Chrome): open the URL, menu (three dots), Install app (or Add to Home screen).
- iPhone (Safari): open the URL, Share, Add to Home Screen.

Open the app once while online. After that it launches from the icon and works in airplane mode.

## Move your existing data

Browser storage is per website address, so data from the preview link will not follow you.

1. In the old app: Settings > Export data, copy the text.
2. In the new installed app: Settings, paste into the box, tap Restore from text.

## Updating later

Edit `index.html` and push to GitHub. The phone refreshes the app in the background when online. Close and reopen the app once or twice to see the new version. If it looks stuck, change `form-v1` to `form-v2` in `sw.js`.

## Keep your data safe

Everything is stored on the phone (localStorage). Install the app to the home screen, and use Settings > Export data now and then, especially before changing phones or clearing browser data.
