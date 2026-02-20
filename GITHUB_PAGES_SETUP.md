# GitHub Pages Setup Guide

## Current Status

✅ **Files Ready:**
- `index.html` - Main HTML file (present)
- `.nojekyll` - Disables Jekyll processing (created)

## Steps to Fix 404 Error

### 1. Enable GitHub Pages

1. Go to your repository: https://github.com/vatsalgoyal/AgriRisk
2. Click on **Settings** (top menu)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select:
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Click **Save**

### 2. Verify Repository is Public

GitHub Pages only works for:
- Public repositories (free)
- Private repositories (requires GitHub Pro/Team)

Make sure your repository is set to **Public**:
1. Go to **Settings** → **General**
2. Scroll to **Danger Zone**
3. If it says "Change visibility", ensure it's set to **Public**

### 3. Wait for Deployment

After enabling GitHub Pages:
- Wait 1-2 minutes for the site to build
- Your site will be available at: `https://vatsalgoyal.github.io/AgriRisk/`
- You can check deployment status in **Settings** → **Pages**

### 4. Verify Files are Committed

Make sure all files are committed and pushed:

```bash
git add .
git commit -m "Add .nojekyll for GitHub Pages"
git push origin main
```

## Troubleshooting

### Still Getting 404?

1. **Check Repository Name:** Ensure it matches exactly: `AgriRisk` (case-sensitive)
2. **Check Branch:** Must be `main` or `master`
3. **Check File Location:** `index.html` must be in the root directory
4. **Clear Browser Cache:** Try incognito/private browsing
5. **Check GitHub Actions:** Go to **Actions** tab to see if there are any build errors

### Common Issues

- **404 Error:** Usually means GitHub Pages isn't enabled or wrong branch selected
- **Blank Page:** Check browser console for JavaScript errors
- **Styling Issues:** Ensure CDN links are accessible (Tailwind CSS, Chart.js)

## File Structure

Your repository should have:
```
AgriRisk/
├── .nojekyll          ← Required for static HTML sites
├── index.html         ← Main page (required)
├── README.md
└── docs/
    └── Auto/
```

## Testing Locally

Before pushing, test locally:
1. Open `index.html` in a browser
2. Check browser console (F12) for errors
3. Verify all CDN resources load correctly

## Deployment Checklist

- [ ] Repository is public
- [ ] GitHub Pages is enabled (Settings → Pages)
- [ ] Source branch is set to `main` and folder to `/ (root)`
- [ ] `.nojekyll` file exists in root
- [ ] `index.html` exists in root
- [ ] All changes are committed and pushed
- [ ] Wait 1-2 minutes after enabling Pages

---

**After completing these steps, your site should be live at:**
**https://vatsalgoyal.github.io/AgriRisk/**
