# Areté — Deploy to Vercel

This is a static, single-file website (`index.html`). Everything — copy,
styling, the snow/fog/dove animation, and the demo member dashboard — lives
in that one file, so it's simple to host and simple to edit.

## Option A — Vercel dashboard (no coding tools needed)

1. Go to https://vercel.com and sign in (or create a free account).
2. Click **Add New... → Project**.
3. Choose **"Deploy without Git"** / drag-and-drop (look for an upload area
   on the New Project screen).
4. Drag this whole folder (or just `index.html`) onto the page.
5. Click **Deploy**. Vercel will give you a live `*.vercel.app` URL in
   under a minute.
6. Later, go to the project's **Settings → Domains** to attach your own
   domain (e.g. aretetrading.com).

## Option B — Vercel CLI

If you're comfortable with a terminal:

```bash
npm install -g vercel
cd path/to/this/folder
vercel login
vercel --prod
```

Follow the prompts (press Enter to accept the defaults — Vercel auto-detects
this as a static site). You'll get a live URL when it finishes.

## Option C — GitHub + Vercel (best if you'll keep editing it)

1. Create a new repository on GitHub and push this folder to it.
2. In Vercel, click **Add New... → Project** and import that GitHub repo.
3. Leave all build settings blank/default — it's a static site, nothing to
   build.
4. Click **Deploy**. Every future push to GitHub will auto-redeploy.

## Editing the site

Open `index.html` in any text editor. Everything is in that one file:
- Copy/text: search for the section you want (hero, pricing, FAQ, etc.)
- Colors: edit the CSS variables near the top (`--bg`, `--fg`, etc.)
- Discord link: already set to https://discord.gg/jmJ84ddrt in a few spots
- Demo dashboard data: see the `localStorage` section near the bottom of
  the `<script>` tag — this is placeholder data until a real backend
  (Discord OAuth + a database) is connected. See the in-page note in the
  "Member dashboard" section for what that would involve.

No build step, no dependencies, no `npm install` required for the current
version — it's a plain HTML/CSS/JS file.
