# Deployment Guide

## Quick Deploy to Vercel via GitHub

### Step 1: Push to GitHub

1. Initialize git (if not already done):
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Airflow Visualization"
   ```

2. Create a new repository on GitHub

3. Push to GitHub:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git branch -M main
   git push -u origin main
   ```

### Step 2: Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign in
2. Click "Add New Project"
3. Import your GitHub repository
4. Vercel will automatically detect it's a Vite project
5. Click "Deploy"

**That's it!** Vercel will:
- Automatically install dependencies (`npm install`)
- Run the build command (`npm run build`)
- Deploy your application

### Vercel Configuration

The project includes `vercel.json` with the correct settings:
- Framework: Vite
- Build Command: `npm run build`
- Output Directory: `dist`

Vercel will auto-detect these settings, so no manual configuration is needed!

### Environment Variables

No environment variables are required for this project. If you need to add any in the future, add them in the Vercel dashboard under Project Settings → Environment Variables.

---

**Note**: You don't need to run `npm install` locally - Vercel handles everything automatically when you push to GitHub!

