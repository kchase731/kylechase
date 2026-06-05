# Kyle Chase — Executive Profile

Static site for **kylechase.com** (or GitHub Pages subdomain).

## Deploy to GitHub Pages

### Option A — New repo (simplest)

```bash
cd kyle-chase-site
git init
git add .
git commit -m "Initial site"
gh repo create kyle-chase --public --source=. --push
```

Then go to **Settings → Pages → Branch: main → / (root) → Save**.

Your site will be live at `https://yourusername.github.io/kyle-chase` within ~60 seconds.

### Option B — Custom domain (kylechase.com)

1. Deploy via Option A first
2. Add `CNAME` file to repo root containing your domain (e.g. `kylechase.com`)
3. In GitHub Pages settings, enter your custom domain
4. At your DNS registrar, add:
   - `A` records pointing to GitHub's IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Or a `CNAME` record: `www → yourusername.github.io`

### Option C — Drag & drop (zero terminal)

Go to [github.com/new](https://github.com/new), create a public repo, then drag `index.html` into the file upload area. Enable Pages in Settings.

## Files

```
kyle-chase-site/
└── index.html    # Everything — single file, no dependencies, no build step
```

Single HTML file. No frameworks. No build step. Loads Google Fonts from CDN, everything else is inline.
