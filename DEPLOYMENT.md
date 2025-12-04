# Deployment Guide for Meshfold AI Website

## Quick Comparison: Vercel vs Netlify

Both platforms are excellent for static sites. Here's a quick comparison:

**Vercel:**
- ✅ Slightly faster global CDN
- ✅ Excellent developer experience
- ✅ Great for modern web apps
- ✅ Automatic HTTPS and custom domains
- ✅ Free tier: 100GB bandwidth/month

**Netlify:**
- ✅ Excellent for static sites
- ✅ Built-in form handling (if needed later)
- ✅ Great developer experience
- ✅ Automatic HTTPS and custom domains
- ✅ Free tier: 100GB bandwidth/month

**Recommendation:** Both are equally good for this project. Choose based on personal preference or existing account.

---

## Option 1: Deploy to Vercel

### Method A: Via Vercel Dashboard (Easiest)

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin <your-github-repo-url>
   git push -u origin main
   ```

2. **Deploy on Vercel:**
   - Go to [vercel.com](https://vercel.com)
   - Sign up/Login with GitHub
   - Click "Add New Project"
   - Import your GitHub repository
   - Vercel will auto-detect it's a static site
   - Click "Deploy"
   - Done! Your site will be live in ~30 seconds

### Method B: Via Vercel CLI

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Follow the prompts
# For production: vercel --prod
```

---

## Option 2: Deploy to Netlify

### Method A: Via Netlify Dashboard (Easiest)

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin <your-github-repo-url>
   git push -u origin main
   ```

2. **Deploy on Netlify:**
   - Go to [netlify.com](https://netlify.com)
   - Sign up/Login with GitHub
   - Click "Add new site" → "Import an existing project"
   - Select your GitHub repository
   - Build settings:
     - Build command: (leave empty)
     - Publish directory: `.` (current directory)
   - Click "Deploy site"
   - Done! Your site will be live in ~1 minute

### Method B: Via Netlify CLI

```bash
# Install Netlify CLI
npm i -g netlify-cli

# Login
netlify login

# Deploy
netlify deploy

# For production: netlify deploy --prod
```

### Method C: Drag & Drop (Quickest for testing)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop your project folder
3. Site is live instantly!

---

## Custom Domain Setup

Both platforms support custom domains:

**Vercel:**
- Go to Project Settings → Domains
- Add your domain (www.meshfoldai.com)
- Follow DNS configuration instructions

**Netlify:**
- Go to Site Settings → Domain Management
- Add your domain (www.meshfoldai.com)
- Follow DNS configuration instructions

---

## Continuous Deployment

Both platforms automatically deploy when you push to GitHub:
- Push to `main` branch → Production deployment
- Push to other branches → Preview deployment

---

## Environment Variables (if needed later)

Both platforms support environment variables in their dashboards.

---

## Recommendation

For this static site, **both are equally good**. I'd suggest:
- **Vercel** if you want the fastest possible CDN
- **Netlify** if you might need forms or serverless functions later

You can also deploy to both and use different domains for A/B testing!

