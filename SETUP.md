# Quick Setup Guide for GitHub Pages

Follow these steps to deploy this experiment to GitHub Pages:

## Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the **+** icon in the top right → **New repository**
3. Name your repository (e.g., `vocab-experiment`)
4. Make it **Public** (required for free GitHub Pages)
5. **Do NOT** initialize with README, .gitignore, or license
6. Click **Create repository**

## Step 2: Initialize Git and Push

Open a terminal in this directory and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Make initial commit
git commit -m "Initial commit: Vocabulary experiment"

# Rename branch to main (if needed)
git branch -M main

# Add your GitHub repository as remote (replace with your actual URL)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Push to GitHub
git push -u origin main
```

**Replace `YOUR_USERNAME` and `YOUR_REPO_NAME` with your actual GitHub username and repository name.**

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub.com
2. Click **Settings** (top menu)
3. Click **Pages** (left sidebar)
4. Under **Source**:
   - Select **Branch**: `main`
   - Select **Folder**: `/ (root)`
5. Click **Save**

## Step 4: Access Your Site

Wait 1-2 minutes, then visit:
```
https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/
```

## Step 5: Configure Experiment (Optional)

1. Edit `index.html`
2. Update `EXPERIMENT_ID` (line ~481) if needed
3. Update vocabulary path (line ~614) to use a different vocabulary size
4. Commit and push changes:
   ```bash
   git add index.html
   git commit -m "Update experiment configuration"
   git push
   ```

## Troubleshooting

- **Site not loading?** Check Settings → Pages to ensure it's enabled
- **404 errors?** Verify file paths match your repository structure
- **JSON not loading?** Check browser console (F12) for errors
- **Changes not appearing?** Wait a few minutes and clear browser cache

## Need Help?

Check the main README.md for more detailed information.

