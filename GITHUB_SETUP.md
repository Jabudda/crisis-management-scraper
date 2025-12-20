# GitHub Repository Setup Instructions

## ✅ Local Repository Ready!

Your git repository has been initialized and all files are committed locally.

## 🌐 Create GitHub Repository

### Option 1: Using GitHub Website (Recommended)

1. **Go to GitHub and create a new repository**
   - Visit: https://github.com/new
   - Repository name: `crisis-management-scraper` (or your preferred name)
   - Description: `Web scraper that monitors current events and ranks by severity`
   - **Leave it EMPTY** - Don't initialize with README, .gitignore, or license
   - Click "Create repository"

2. **Push your local code to GitHub**
   
   Copy and run these commands (GitHub will show them after creating the repo):
   ```bash
   cd "/Users/jabudda/Crisis Management Web Scraper"
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages**
   - Under **Source**, select:
     - Branch: `main`
     - Folder: `/docs`
   - Click **Save**

4. **Configure GitHub Actions Permissions**
   - Go to **Settings** → **Actions** → **General**
   - Scroll to **Workflow permissions**
   - Select: ✅ **Read and write permissions**
   - Check: ✅ **Allow GitHub Actions to create and approve pull requests**
   - Click **Save**

5. **Your site will be live at:**
   ```
   https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/
   ```

---

### Option 2: Install GitHub CLI (Optional)

If you prefer command-line:

1. **Install GitHub CLI**
   ```bash
   brew install gh
   ```

2. **Authenticate**
   ```bash
   gh auth login
   ```

3. **Create repository and push**
   ```bash
   cd "/Users/jabudda/Crisis Management Web Scraper"
   gh repo create crisis-management-scraper --public --source=. --remote=origin --push
   ```

4. **Enable GitHub Pages**
   ```bash
   gh repo edit --enable-pages --pages-branch=main --pages-path=/docs
   ```

---

## 📝 After Creating Repository

### Update Repository Links

Once created, update these files with your actual repository URL:

1. **README.md** - Replace `YOUR_USERNAME/YOUR_REPO` with actual values
2. **DEPLOYMENT.md** - Update repository URL examples
3. **docs/app.js** - If needed, update the data URL path

### Test the GitHub Actions Workflow

After pushing:
1. Go to the **Actions** tab on GitHub
2. Click **Scrape Crisis Events** workflow
3. Click **Run workflow** to test it manually
4. Verify it runs successfully and updates `data/events.json`

### Verify GitHub Pages

Wait 1-2 minutes after enabling Pages, then visit:
```
https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/
```

You should see your Crisis Management Dashboard live!

---

## 🎯 Current Status

- ✅ Git repository initialized
- ✅ All files committed locally
- ✅ Ready to push to GitHub
- ⏳ Awaiting GitHub repository creation
- ⏳ GitHub Pages setup pending

## 🔗 Quick Reference

**Repository URL format:**
```
https://github.com/YOUR_USERNAME/crisis-management-scraper
```

**GitHub Pages URL format:**
```
https://YOUR_USERNAME.github.io/crisis-management-scraper/
```

**Clone URL format:**
```
https://github.com/YOUR_USERNAME/crisis-management-scraper.git
```

---

## ⚡ Next Steps

1. Create the GitHub repository (Option 1 or 2 above)
2. Push your code
3. Enable GitHub Pages
4. Configure Actions permissions
5. Visit your live dashboard!

Need help? Check [DEPLOYMENT.md](DEPLOYMENT.md) for detailed instructions.
