# SIVEP Project Showcase

Public landing page for LinkedIn — project details + live demo video.

## Preview locally

```powershell
.\scripts\serve_showcase.ps1
```

Open http://localhost:8080

## Publish (get a public URL for LinkedIn)

1. Edit `config.json` → set your real `public_url` (e.g. GitHub Pages)
2. Push the repo to GitHub
3. Enable **GitHub Pages** → source: `/docs` folder or `/docs/showcase`
4. Re-run: `python scripts/generate_showcase.py`

### GitHub Pages (recommended)

- Push repo to GitHub
- Settings → Pages → Deploy from branch `main`, folder `/docs/showcase` or use root `docs/showcase/index.html` via custom workflow
- Your URL: `https://<username>.github.io/<repo>/showcase/`

### Netlify Drop (fastest, no git)

1. Zip the `docs/showcase/` folder (with `assets/`)
2. Go to https://app.netlify.com/drop
3. Paste the URL in `config.json` and regenerate LinkedIn post

## Add demo video

Place `demo_live.mp4` in `docs/linkedin/media/` then run:

```powershell
python scripts/generate_showcase.py
python scripts/generate_linkedin_pack.py
```

## Current public URL

**https://sihadi.github.io/sivep/**

Update `docs/showcase/config.json` before publishing on LinkedIn.
