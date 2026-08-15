# Eastern Shore Smart Listings — Website

A single-page site: hero, three service highlights, and a contact section
(form + direct email/phone). No backend required — hosting and the contact
form are both free.

## Files
- `index.html` — the page
- `styles.css` — all styling
- `script.js` — footer year only
- `success.html` — shown after someone submits the contact form
- `netlify.toml` — tells Netlify this is a plain static site (no build step)

## 1. Before you deploy: swap the placeholders
Open `index.html` and search for these and replace with your real info:
- `hello@easternshoresmartlistings.com` (appears twice — once as link text, once in `href="mailto:..."`)
- `(251) 555-0123` and `tel:+12515550123`
- The "Placeholder contact details" note can be deleted once real info is in.

## 2. Put it on GitHub
1. Create a new **public or private** repo on github.com (e.g. `eastern-shore-smart-listings`).
2. On your machine, in this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```
   (Or use GitHub Desktop / the "upload files" button on github.com if you'd rather not use the command line.)

## 3. Connect Netlify to that repo
1. Go to [app.netlify.com](https://app.netlify.com) and sign up/log in with your **GitHub account** — this is what links them together.
2. Click **Add new site → Import an existing project → Deploy with GitHub**.
3. Pick your repo.
4. Build settings: leave **Build command** blank and **Publish directory** as `.` (root) — `netlify.toml` already sets this, so Netlify should pick it up automatically.
5. Click **Deploy**. You'll get a free URL like `random-name-123.netlify.app` within a minute or so.
6. Optional: in **Site settings → Site details → Change site name**, pick something like `eastern-shore-smart-listings.netlify.app`.

From now on, every push to `main` on GitHub auto-deploys to that URL — no extra steps.

## 4. Contact form — nothing extra to set up
The form uses **Netlify Forms**, which is free and built in. Netlify detects
the `data-netlify="true"` form automatically on deploy. Submissions show up
under your site's **Forms** tab in the Netlify dashboard, and you can turn on
free email notifications there too:
**Site settings → Forms → Form notifications → Add notification → Email
notification** → enter the address you want submissions sent to.

There's also a hidden honeypot field already in the form to cut down on spam
bots, no extra service needed.

## 5. When you're ready for a real domain
**Site settings → Domain management → Add a custom domain** in Netlify — you
can point a domain you buy elsewhere at your Netlify site, or buy one through
Netlify directly. Everything else about the site stays the same.

## Notes / things you might want next
- The AI-staging/walkthrough example images in your flyer aren't on the site
  yet — once you have real before/after examples, a small gallery under
  Services would probably do more to convert visitors than anything else here.
- Consider a one-line disclosure near any AI-staged photos you add later
  (a version is already in the footer) — some MLS/brokerage rules require
  disclosing AI-generated imagery.
