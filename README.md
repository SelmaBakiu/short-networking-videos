# Network Layer in 16 Reels: deployable site

A static website: no server code, no build step. Upload this folder as it is.

## Contents
- `index.html`: the swipe player (TikTok-style)
- `videos/part01.mp4` … `part16.mp4`: the videos
- `videos/part01.jpg` … `part16.jpg`, `videos/poster.jpg`: preview images
- `videos/videos.js`: the list of videos (titles, captions, episodes); edit this to rename or add videos

## Deploy (pick one)

**Netlify (easiest, no account setup needed beyond sign-in)**
1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page. You get a public link in seconds.

**GitHub Pages**
1. Create a new repository and upload all files (keep the `videos` folder).
2. Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. Your site appears at `https://<your-username>.github.io/<repo-name>/`.

**Vercel**
1. `npm i -g vercel`, then run `vercel` inside this folder (choose "Other" / no framework).

**Any web host / test locally**
- Copy the folder to any static host (Cloudflare Pages, S3, your own server).
- Local test: `python3 -m http.server 8000` in this folder, then open http://localhost:8000
  (opening index.html directly as a file also works in most browsers).

## Adding a video
1. Put `part17.mp4` (and an optional `part17.jpg`) in `videos/`.
2. Add an entry to `videos/videos.js`:
   `{ "ep": 9, "part": 1, "of": 1, "n": 17, "title": "My new video", "text": "Caption", "file": "videos/part17.mp4" }`
3. Optionally add `"9": "Episode 9 · Topic"` to `EP_TITLES`.
