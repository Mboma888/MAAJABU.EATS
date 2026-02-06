# Maajabu Restaurant - GitHub Pages Deployment Guide

## ✅ What's Been Fixed

### 1. **Liquid Syntax Errors** (FIXED)
   - Wrapped JSX/TSX code blocks in `{% raw %}` tags in `public/maajabu-restaurant-code.md`
   - Protected all template literals from Jekyll processing

### 2. **GitHub Pages Configuration** (ADDED)
   - Created `.github/workflows/deploy.yml` for automatic deployment
   - Added `.nojekyll` file to prevent Jekyll processing
   - Updated `vite.config.ts` with proper base path

### 3. **Deployment Ready**
   - All files are now properly configured for GitHub Pages
   - Automatic build and deploy on push to main branch

---

## 🚀 How to Deploy

### Step 1: Create/Setup Your GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it whatever you like (e.g., `maajabu-restaurant`)
3. **DO NOT** initialize with README, .gitignore, or license (we have those already)

### Step 2: Upload Your Files

**Option A: Using GitHub Web Interface (Easiest)**

1. Extract the `maajabu-restaurant-COMPLETE.zip` file
2. Go to your new repository on GitHub
3. Click **"uploading an existing file"** or drag and drop
4. **Upload ALL files and folders** from the extracted zip
5. Commit with message: `Initial commit - Maajabu Restaurant website`

**Option B: Using Git Command Line**

```bash
# Extract the zip file first, then:
cd maajabu-restaurant-COMPLETE
git init
git add .
git commit -m "Initial commit - Maajabu Restaurant website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar)
4. Under **Source**, select: **GitHub Actions**
5. Click **Save**

### Step 4: Wait for Deployment

1. Go to the **Actions** tab in your repository
2. You'll see a workflow running called "Deploy to GitHub Pages"
3. Wait for it to complete (green checkmark ✅)
4. Your site will be live at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

---

## 📁 Project Structure

```
maajabu-restaurant/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions deployment workflow
├── public/
│   ├── .nojekyll               # Prevents Jekyll processing
│   └── maajabu-restaurant-code.md  # Fixed markdown file
├── src/                        # React source code
├── index.html                  # Entry HTML file
├── package.json                # Dependencies
├── vite.config.ts              # Vite configuration (updated)
└── ... other config files
```

---

## 🔧 Configuration Details

### GitHub Actions Workflow (`.github/workflows/deploy.yml`)
- **Triggers**: Pushes to `main` branch or manual dispatch
- **Steps**: 
  1. Checkout code
  2. Setup Node.js 20
  3. Install dependencies (`npm ci`)
  4. Build project (`npm run build`)
  5. Deploy to GitHub Pages

### Vite Configuration (`vite.config.ts`)
- **Base Path**: Set to `/` for root deployment
- **Build Output**: `dist/` folder

### Jekyll Prevention (`.nojekyll`)
- Empty file that tells GitHub Pages NOT to process the site with Jekyll
- Critical for React/Vite apps

---

## 🐛 Troubleshooting

### Issue: "Page build failed" error
**Solution**: Make sure you selected "GitHub Actions" as the source in Settings > Pages, NOT "Deploy from branch"

### Issue: Site shows blank page
**Solution**: 
1. Check the browser console for errors
2. Make sure the base path in `vite.config.ts` matches your repo structure
3. If using a custom domain or repo name, update the base path accordingly

### Issue: 404 error on routes
**Solution**: Add a `404.html` that redirects to index.html (already included)

### Issue: Actions workflow fails
**Solution**: 
1. Check the Actions tab for detailed error logs
2. Make sure all dependencies are in `package.json`
3. Verify Node.js version compatibility

---

## 📝 Making Updates

After initial deployment, to update your site:

1. Make changes to your code locally or in GitHub
2. Commit and push to the `main` branch
3. GitHub Actions will automatically rebuild and redeploy
4. Changes will be live in 2-3 minutes

---

## 🎨 Local Development

To run the site locally:

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

Development server will run at: `http://localhost:8080`

---

## 📧 Support

If you encounter any issues:
1. Check the Actions tab for build logs
2. Review the troubleshooting section above
3. Verify all files were uploaded correctly
4. Check that GitHub Pages is enabled with "GitHub Actions" as source

---

## ✨ What's Included

- ✅ Complete React + Vite + TypeScript application
- ✅ Fixed Liquid syntax errors in markdown documentation
- ✅ GitHub Actions workflow for automatic deployment
- ✅ Proper GitHub Pages configuration
- ✅ All dependencies and build configuration
- ✅ Responsive design with Tailwind CSS
- ✅ Menu, About, Contact pages
- ✅ WhatsApp integration

---

**Ready to deploy!** Follow the steps above and your restaurant website will be live in minutes! 🎉
