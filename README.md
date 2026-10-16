# Amharic Input

A simple website for Amharic comprehensible-input videos: video library, streak tracker, premium access, and a method page. No build tools. It's plain HTML, CSS and JavaScript.

## Put it on GitHub and the web
1. Create a free account at github.com, then click **New repository** (name it e.g. `amharic-input`).
2. Click **uploading an existing file** and drag in everything from this folder. Commit.
3. Go to **Settings > Pages**, set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io/amharic-input/`.

To test on your computer first, just double-click `index.html`.

## Add a video
1. Put the `.mp4` in the `videos/` folder (H.264 video + AAC audio plays everywhere).
2. Open `js/videos.js` and copy one video block. Change `id`, `title`, `level`, `file`, etc.
3. Optional: add a thumbnail image and set `thumb: "videos/mything.jpg"`.
4. Commit. The site updates itself.

## Settings (in `js/videos.js`)
- `dailyGoalMinutes`: minutes per day needed to keep the streak.
- `paymentLink`: paste a Stripe Payment Link, Gumroad or Ko-fi link.
- `premiumCodes`: codes you email to people after they pay.

## Honest limitations (good to know now)
- **Premium is a soft lock.** The site is static, so a technical person could find the video files or the codes. Fine for a start with friends and early customers. For real protection, move to Supabase (accounts) plus Stripe, and host videos on private storage. Your dad could help with that step.
- **Streaks live in each person's browser.** Clearing browser data or switching devices resets them. Real accounts fix this later.
- **GitHub limits:** files over 100 MB can't be uploaded through the website, and repos should stay under about 1 GB. Once you have many videos, host them on Cloudflare R2 or Bunny Stream and put the full URL in `file:`.
