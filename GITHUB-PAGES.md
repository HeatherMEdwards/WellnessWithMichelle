# GitHub Pages — why the site might not be showing

## Most likely cause: Pages isn't enabled

GitHub Pages is **off by default**. The site will 404 until you turn it on.

### Enable Pages (repo admin)

1. Open the repo on GitHub → **Settings**.
2. In the left sidebar, under **"Code and automation"**, click **Pages**.
3. Under **"Build and deployment"** → **Source**, choose **Deploy from a branch**.
4. Under **Branch**:
   - Branch: **main** (or **master** if that's your default).
   - Folder: **/ (root)**.
5. Click **Save**.

After a few minutes the site should be at:

- **Project site:** `https://<owner>.github.io/WellnessWithMichelle/`  
  e.g. `https://heatheredwards.github.io/WellnessWithMichelle/`

## Checklist if it still doesn't work

- **Publishing source:** An admin with a **verified email** must have pushed to the branch you chose (e.g. `main`). Unverified accounts can block deployment.
- **Correct branch/folder:** The branch and folder in Settings must match where `index.html` lives (here: root of `main`).
- **Wait:** Allow **~5–10 minutes** after saving Settings or pushing changes.
- **Cache:** Try a private/incognito window or a different browser if you still see an old 404.
- **Actions:** In the **Actions** tab, check for a **"pages build and deployment"** workflow; if it failed, open the run for error details.

## Repo setup (already done)

- `index.html` is at the repo root.
- `.nojekyll` is in the repo so GitHub serves the site as plain static files (no Jekyll build).

Once **Settings → Pages → Deploy from a branch** is set and saved, the site should appear at the URL above.
