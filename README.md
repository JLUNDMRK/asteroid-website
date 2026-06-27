# Asteroid — public website

Static site for [asteroid.jlundmark.org](https://asteroid.jlundmark.org), hosted on **GitHub Pages**.

| URL | Page |
|-----|------|
| `/` | Landing page (logo + Play link when live) |
| `/privacy/` | Privacy policy (Google Play) |
| `/terms/` | Terms of service |

## Publish to GitHub

### 1. Create the repository

```bash
cd asteroid-website
git init
git add .
git commit -m "Add Asteroid landing page, privacy, and terms"
gh repo create JLUNDMRK/asteroid-website --public --source=. --remote=origin --push
```

(Or create an empty repo `asteroid-docs` on GitHub and push to it.)

### 2. Enable GitHub Pages

1. Repository **Settings → Pages**
2. **Source:** Deploy from branch `main`, folder `/ (root)`
3. **Custom domain:** `asteroid.jlundmark.org` → Save (creates/updates `CNAME`)
4. Enable **Enforce HTTPS** when DNS is verified

### 3. Cloudflare DNS

On `jlundmark.org`:

| Type | Name | Target | Proxy |
|------|------|--------|-------|
| CNAME | `asteroid` | `jlundmrk.github.io` | Proxied (orange cloud) |

Use your GitHub username/org if different from `jlundmrk`.

### 4. Play Console

- **Privacy policy URL:** `https://asteroid.jlundmark.org/privacy/`
- Optional terms URL: `https://asteroid.jlundmark.org/terms/`

## When Google Play is live

In `index.html`, replace the &quot;Coming soon&quot; badge with the Play Store link (comment in file shows the markup).

## App link

Update the Android app `project_docs_url` to:

`https://asteroid.jlundmark.org/privacy/`
