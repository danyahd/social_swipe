# Deploying Social Swipe Website to Vercel

This guide will help you deploy your Social Swipe website to Vercel for free.

## 🚀 Quick Start (Recommended)

### Option 1: Deploy via Vercel CLI (Fastest)

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**
   ```bash
   vercel login
   ```
   - Follow the prompts to authenticate (email or GitHub)

3. **Deploy from the website folder**
   ```bash
   cd website
   vercel
   ```

4. **Follow the prompts:**
   - Set up and deploy? `Y`
   - Which scope? (Select your account)
   - Link to existing project? `N`
   - What's your project's name? `social-swipe` (or any name you prefer)
   - In which directory is your code located? `./` (current directory)
   - Want to override settings? `N`

5. **Production Deployment**
   ```bash
   vercel --prod
   ```

6. **Done!** Your site will be live at: `https://social-swipe.vercel.app`

---

## Option 2: Deploy via Vercel Dashboard (Easiest for Beginners)

### Step 1: Create a GitHub Repository (Recommended)

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it: `social-swipe-website`
3. Keep it public or private (your choice)
4. Don't initialize with README (we already have files)

### Step 2: Push Website to GitHub

Open terminal in the `website/` folder and run:

```bash
cd website
git init
git add .
git commit -m "Initial commit: Social Swipe website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/social-swipe-website.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your actual GitHub username.

### Step 3: Deploy to Vercel

1. **Go to [Vercel](https://vercel.com)**
2. **Sign Up / Login** (use GitHub account for easier integration)
3. **Click "Add New Project"**
4. **Import Git Repository:**
   - Click "Import" next to your `social-swipe-website` repository
   - If you don't see it, click "Import Git Repository" and paste the URL

5. **Configure Project:**
   - **Project Name:** `social-swipe` (or your preference)
   - **Framework Preset:** Leave as "Other" or select "Static Site"
   - **Root Directory:** `./` (leave default)
   - **Build Command:** Leave empty (static site, no build needed)
   - **Output Directory:** Leave empty or set to `./`
   - **Install Command:** Leave empty

6. **Click "Deploy"**

7. **Wait 30-60 seconds** for deployment to complete

8. **Done!** Your site will be live at:
   - `https://social-swipe.vercel.app` (auto-generated)
   - Or your custom domain once configured

---

## Option 3: Drag & Drop (No Git Required)

1. **Go to [Vercel](https://vercel.com)**
2. **Sign Up / Login**
3. **Click "Add New Project"**
4. **Select "Upload" tab**
5. **Drag and drop the `website/` folder** onto the upload area
6. **Configure:**
   - Project Name: `social-swipe`
   - Click "Deploy"
7. **Done!** Site deployed in seconds

---

## 🌐 Custom Domain Setup (socialswipe.online)

### After Initial Deployment:

1. **Go to your Vercel project dashboard**
2. **Click "Settings" > "Domains"**
3. **Add domain:** `socialswipe.online`
4. **Vercel will provide DNS records:**

   ```
   Type: A
   Name: @
   Value: 76.76.19.19

   Type: CNAME
   Name: www
   Value: cname.vercel-dns.com
   ```

5. **Go to your domain registrar** (where you bought socialswipe.online)
6. **Add these DNS records** in your domain's DNS settings
7. **Wait 24-48 hours** for DNS propagation (usually faster, 1-2 hours)
8. **Done!** Your site will be accessible at:
   - `https://socialswipe.online`
   - `https://www.socialswipe.online`

### SSL Certificate:
- ✅ Vercel automatically provides free SSL certificates
- ✅ Your site will be HTTPS by default

---

## 📁 Files Ready for Deployment

Your `website/` folder contains:

```
website/
├── index.html          # Main landing page (auto-serves at /)
├── landing-page.html   # Backup/original name
├── help.html           # Help documentation page
├── privacy.html        # Privacy policy page
├── vercel.json         # Vercel configuration
└── images/             # Screenshots and promotional images
    ├── image1.png
    ├── image7.png
    ├── image8.png
    ├── image9.png
    └── ...
```

---

## ✅ Vercel Configuration Explained

The `vercel.json` file is configured for:
- ✅ Serve `index.html` as the homepage
- ✅ Clean URLs (no `.html` extensions needed)
- ✅ Proper routing for all pages

**What this means:**
- `socialswipe.online/` → serves `index.html`
- `socialswipe.online/help` → serves `help.html`
- `socialswipe.online/privacy` → serves `privacy.html`

---

## 🔄 Updating Your Website

### If using Git/GitHub:

1. Make changes to files in `website/` folder
2. Commit and push to GitHub:
   ```bash
   cd website
   git add .
   git commit -m "Update website"
   git push
   ```
3. **Vercel automatically deploys** the changes!
4. Live in 30-60 seconds

### If using CLI:

```bash
cd website
vercel --prod
```

### If using Drag & Drop:

- Drag the updated folder to Vercel dashboard again

---

## 🧪 Preview Deployments

Every push to GitHub creates a **preview deployment** with a unique URL:
- Test changes before going live
- Share with team for feedback
- Automatic for every branch/PR

---

## 📊 Vercel Features You Get (Free)

✅ **Unlimited bandwidth**
✅ **Automatic SSL certificates**
✅ **Global CDN** (fast worldwide)
✅ **Automatic HTTPS**
✅ **Custom domains** (including socialswipe.online)
✅ **Preview deployments**
✅ **Analytics** (basic)
✅ **99.99% uptime**
✅ **Automatic deployments** from Git

---

## 🐛 Troubleshooting

### Images not loading?
- Check that `images/` folder is in the same directory as `index.html`
- Verify image paths are relative: `images/image1.png` (not `/images/...`)

### Pages showing 404?
- Ensure `vercel.json` is in the root of the `website/` folder
- Check file names are lowercase and match links

### CSS not applying?
- Check that inline styles in HTML files are correct
- Clear browser cache (Ctrl + F5)

### Domain not working?
- Wait 24-48 hours for DNS propagation
- Verify DNS records are correct in your registrar
- Use [DNS Checker](https://dnschecker.org) to verify propagation

---

## 🎯 After Deployment Checklist

- [ ] Website loads at Vercel URL
- [ ] All pages accessible (index, help, privacy)
- [ ] Images display correctly
- [ ] Links work properly
- [ ] SSL certificate active (HTTPS)
- [ ] Custom domain configured (if ready)
- [ ] Test on mobile devices
- [ ] Share URL in Chrome Web Store listing

---

## 📞 Need Help?

- **Vercel Documentation:** https://vercel.com/docs
- **Vercel Support:** https://vercel.com/support
- **Community:** https://github.com/vercel/vercel/discussions

---

## 🚀 Quick Commands Reference

```bash
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy (development)
cd website
vercel

# Deploy to production
vercel --prod

# Check deployment status
vercel ls

# Remove deployment
vercel rm [deployment-url]
```

---

Your website is now ready to deploy! Choose the method that works best for you and let's get Social Swipe online! 🎉
