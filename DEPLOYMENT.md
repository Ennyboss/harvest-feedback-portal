# GitHub Pages Deployment Guide

Complete step-by-step instructions to deploy the HARVEST Tool Feedback Portal to GitHub Pages.

## Prerequisites

- Git installed on your machine
- GitHub account with access to the `Ennyboss/harvest-feedback-portal` repository
- All project files committed and ready to push

## Current Project Structure

The project is already structured correctly for GitHub Pages:
```
harvest-feedback-portal-main/
├── index.html                    # Main entry point
├── icicle-logo.jpg               # Logo image
├── Harvest_In_5_Steps_Guide.pdf  # PDF guide
├── .nojekyll                     # Ensures proper file serving
└── README.md                     # Documentation
```

**Important**: `index.html` is already at the repository root, which is perfect for GitHub Pages.

## Step 1: Git Commands (Terminal)

Run these commands in your terminal from the project directory:

```bash
# Navigate to your project directory (where the .git folder is)
# This should be: harvest-feedback-portal-main/harvest-feedback-portal-main/
cd harvest-feedback-portal-main/harvest-feedback-portal-main

# Check current status
git status

# Add all files (including .nojekyll and updated README)
git add .

# Commit the changes
git commit -m "Add .nojekyll file and update README for GitHub Pages deployment"

# Verify remote is set correctly
git remote -v
# Should show: origin  https://github.com/Ennyboss/harvest-feedback-portal.git

# Push to main branch (this is what GitHub Pages will deploy from)
git push origin main
```

**Note**: If you haven't initialized git yet, run these first:
```bash
git init
git remote add origin https://github.com/Ennyboss/harvest-feedback-portal.git
git branch -M main
```

## Step 2: Enable GitHub Pages (GitHub Web UI)

1. **Go to your repository** on GitHub:
   - Navigate to: https://github.com/Ennyboss/harvest-feedback-portal

2. **Open Settings**:
   - Click on the **"Settings"** tab at the top of the repository

3. **Navigate to Pages**:
   - In the left sidebar, scroll down and click **"Pages"**
   - (It's under the "Code and automation" section)

4. **Configure Source**:
   - Under **"Source"**, click the dropdown that says **"None"** or **"Deploy from a branch"**
   - Select **"Deploy from a branch"**

5. **Select Branch and Folder**:
   - **Branch**: Select `main` from the first dropdown
   - **Folder**: Select `/ (root)` from the second dropdown
   - Click **"Save"**

6. **Wait for Deployment**:
   - You'll see a message: "Your site is ready to be published at..."
   - GitHub will start building your site (this takes 1-2 minutes)
   - You'll see a green checkmark when it's deployed

## Step 3: Access Your Site

Once deployment is complete:

- **Your live site URL**: `https://ennyboss.github.io/harvest-feedback-portal/`
- GitHub will display this URL in the Pages settings section
- You can also find it in the repository's "About" section (you can add it there)

## Important Notes

### GitHub Pages Specific Considerations:

1. **Index File Required**: ✅ Your `index.html` is already at the root - perfect!

2. **The `.nojekyll` File**: 
   - This file tells GitHub Pages NOT to use Jekyll processing
   - Important for serving PDF files and other static assets correctly
   - Already created in your project

3. **First Deploy Time**: 
   - The first deployment typically takes 2-5 minutes
   - Subsequent updates are usually faster (1-2 minutes)

4. **Automatic Deployments**:
   - Every time you push to the `main` branch, GitHub Pages will automatically rebuild and deploy your site
   - You can monitor deployments in: **Settings → Pages → Build and deployment**

5. **Custom Domain** (Optional):
   - If you want a custom domain, you can configure it in **Settings → Pages → Custom domain**
   - You'll need to add DNS records pointing to GitHub Pages

## Troubleshooting

### Site Not Loading:
- Wait a few minutes after enabling Pages
- Check **Settings → Pages** for any error messages
- Verify `index.html` is in the repository root
- Ensure the branch is `main` and folder is `/ (root)`

### Assets Not Loading:
- Make sure `.nojekyll` file exists (prevents Jekyll from processing files)
- Verify image/PDF paths in `index.html` use relative paths (e.g., `icicle-logo.jpg`, not `/icicle-logo.jpg`)
- Check file names match exactly (case-sensitive on GitHub Pages)

### Updates Not Showing:
- Clear your browser cache (Ctrl+Shift+R or Cmd+Shift+R)
- Check the deployment status in **Settings → Pages**
- Verify you pushed to the `main` branch

## Verification Checklist

After deployment, verify:

- [ ] Site is accessible at `https://ennyboss.github.io/harvest-feedback-portal/`
- [ ] Logo image displays correctly
- [ ] PDF viewer loads the guide
- [ ] All survey links work
- [ ] Site is responsive on mobile devices
- [ ] YouTube videos embed correctly

## Next Steps

After successful deployment:

1. Test all functionality on the live site
2. Share the URL with stakeholders
3. Monitor feedback through the Google Forms
4. Make updates by editing files locally and pushing to `main` branch

---

**Questions or Issues?** Check GitHub Pages documentation: https://docs.github.com/en/pages

