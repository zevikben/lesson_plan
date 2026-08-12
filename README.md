# Weekly Lesson Plan — deployment guide

This is a self-contained offline-capable web app (PWA). Everything runs
entirely on your iPhone once installed — no server, no ongoing internet
connection, no account needed.

## What's in this folder
- `index.html` — the whole app (UI + logic)
- `manifest.json` — tells iOS how to install it as an app icon
- `service-worker.js` — caches the app so it loads with zero internet
- `icons/` — app icon images

## One-time setup: put these files on the web (free, ~10 minutes)

iOS requires a real web address (even briefly) to install a PWA — you can't
install straight from a local file. **GitHub Pages** is the easiest free
way to do this:

1. Go to [github.com](https://github.com) and create a free account if you
   don't have one.
2. Click **New repository** → name it anything (e.g. `lesson-plan`) →
   **Create repository**.
3. On the repository page, click **Add file → Upload files**, and drag in
   all the files from this folder (`index.html`, `manifest.json`,
   `service-worker.js`, and the whole `icons` folder). Commit the upload.
4. Go to **Settings → Pages** (left sidebar). Under **Source**, choose
   **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
5. Wait about a minute, then refresh — GitHub will show you a URL like:
   `https://yourusername.github.io/lesson-plan/`

## Installing on your iPhone

1. Open that URL in **Safari** on your iPhone (must be Safari, not Chrome).
2. Tap the **Share** button (square with an arrow, bottom of the screen).
3. Scroll down and tap **Add to Home Screen**.
4. Tap **Add**.

You'll now have an app icon on your home screen. Open it once while you
still have internet, so it can save its files for offline use — after
that, you can turn on Airplane Mode and it keeps working completely.

## Using the app
- Tap any hour to open it, write your lesson notes, and attach a song.
- **Add new MP3**: pick an audio file from your phone (e.g. from Files, or
  something you've already downloaded) — it's saved permanently inside
  the app from then on, so you never need to add that same song twice.
- **Choose from library**: reuse a song you've already added to any other hour.
- **Reuse a previous lesson**: copies the text + song from any other hour
  you've already filled in, as a starting point you can still edit.
- **Save to your library**: give a lesson its own name (e.g. "Intro to
  Fractions") and it's kept indefinitely, separate from any specific hour
  - reuse it under **Browse your saved lessons** any time, even weeks
  later, without it ever being overwritten the way an hour's content is
  when that same hour comes around again next week.
- Everything is saved automatically on your phone and stays there even
  after closing the app, restarting your phone, or going offline.

## Preparing on your laptop, then using it on your phone
The app also runs in an ordinary browser, not just as an installed app —
so you can open the same GitHub Pages URL on your laptop, plan the whole
week there (bigger screen, real keyboard), and then move it to your phone:

1. On your laptop, open the app in the browser and fill in the week.
2. Tap **Transfer** → **Export file…**. On a Mac in Safari or Chrome, this
   opens the normal macOS Share menu with **AirDrop right there** — pick
   your iPhone and it's sent directly, no folders or cloud services
   involved. (If sharing isn't available in your browser, it falls back
   to downloading one file with everything — all lessons, songs, and
   settings — which you can then send over however you like: AirDrop it
   manually from Downloads, email it, or save it to iCloud Drive/Files.)
3. If you used AirDrop, accept it on the iPhone and choose **Save to
   Files** when prompted.
4. On your phone, open the installed app, tap **Transfer** → **Import
   file…**, and choose the file. This replaces whatever was already on
   the phone with what you exported, so do this before you start editing
   on the phone directly.

You can also export from the phone and import back on the laptop the same
way — it works in either direction.

## Ready / Edit mode
Once a week's plan is finished, tap **Ready** in the top right. The app
switches to a clean, view-only display: notes and songs are still all
there and playable, but nothing can be added, edited, or removed — handy
so a final version can be handed off or displayed without stray taps
changing it. Tap **Edit** to switch back to the normal editing screen at
any time. This state is remembered on the device, and if you export while
in Ready mode, the imported copy on the other device opens in Ready mode
too.

## Updating the app later
If you (or I) change any of these files, re-upload them to the same
GitHub repository (Add file → Upload files, overwrite). Next time you
open the app with internet on, it'll pick up the update automatically.
