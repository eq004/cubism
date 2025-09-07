# Deploy to Netlify (No Local Installs)

This project is a Vite app. Netlify Drop **won't** work with this ZIP because Vite must build the site.

## Option A — *New site from Git* (Recommended)
1. Go to https://github.com → **New repository** → create it.
2. Click **"uploading an existing file"**. Drag in the **contents** of this folder (keep the folder structure).
3. Commit the upload.
4. Go to https://app.netlify.com → **New site from Git** → choose your repo.
5. Deploy. Netlify reads `netlify.toml` and runs:
   - `npm ci && npm run build`
   - Publishes the `dist` folder.

## Option B — *Netlify Drop* with a built folder
1. Open https://stackblitz.com → **Upload project** → select this project folder.
2. In the StackBlitz terminal:
   ```
   npm install
   npm run build
   ```
3. Download the generated **`dist/`** folder.
4. Zip the **contents** of `dist` (so the zip has `index.html` at root).
5. Go to https://app.netlify.com/drop and drop that built zip.

---

**Node version:** set to `20` (configured in `netlify.toml`).  
**Publish directory:** `dist` (Vite default).

Generated: 2025-09-07T11:41:07.136258
