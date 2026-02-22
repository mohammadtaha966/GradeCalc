# 🚀 GradeCalc - Deployment Guide

## 📋 **Quick Fix for Local Testing**

### **Problem:**
Navigation between pages not working locally.

### **Solution:**
All files must be in the **same folder** and opened through a local server.

---

## ✅ **Step 1: Verify Your Files**

Make sure you have these 6 files in ONE folder:

```
gradecalc/
├── index.html (or index-complete.html - rename to index.html)
├── cgpa.html
├── goals.html
├── analytics.html
├── guides.html
└── about.html
```

**IMPORTANT:** Rename `index-complete.html` to `index.html`

---

## 🖥️ **Step 2: Test Locally**

### **Option A: Python Server (Recommended)**

1. Open Terminal/Command Prompt
2. Navigate to your folder:
   ```bash
   cd path/to/your/gradecalc/folder
   ```

3. Start server:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # OR Python 2
   python -m SimpleHTTPServer 8000
   ```

4. Open browser: `http://localhost:8000`

5. Click around - all pages should work!

### **Option B: VS Code Live Server**

1. Install "Live Server" extension in VS Code
2. Right-click `index.html`
3. Select "Open with Live Server"

### **Option C: Node.js (if installed)**

```bash
npx http-server -p 8000
```

---

## 🌐 **Step 3: Deploy Online (FREE)**

### **🎯 METHOD 1: Netlify (EASIEST - Recommended)**

**Perfect for beginners!**

1. **Go to:** https://netlify.com
2. **Sign up** (free - use GitHub, Google, or email)
3. **Drag & Drop Deployment:**
   - Go to https://app.netlify.com/drop
   - Drag your entire `gradecalc` folder into the box
   - Wait 30 seconds
   - **DONE!** You get a live URL like: `your-site.netlify.app`

4. **Custom Domain (Optional):**
   - Go to Site Settings → Domain Management
   - Add your custom domain

**Pros:** Instant, no configuration, free SSL, custom domains
**Cons:** None!

---

### **🎯 METHOD 2: GitHub Pages (FREE)**

**Best for version control**

#### **Step 1: Create GitHub Account**
- Go to https://github.com
- Sign up (free)

#### **Step 2: Create Repository**
1. Click **"+"** (top right) → **"New repository"**
2. Repository name: `gradecalc`
3. Make it **Public**
4. Click **"Create repository"**

#### **Step 3: Upload Files**
1. On the repository page, click **"uploading an existing file"**
2. Drag all 6 HTML files
3. Click **"Commit changes"**

#### **Step 4: Enable GitHub Pages**
1. Go to **Settings** (in your repo)
2. Click **"Pages"** (left sidebar)
3. Under "Source", select **"main"** branch
4. Click **"Save"**
5. Wait 1-2 minutes
6. Your site will be at: `https://yourusername.github.io/gradecalc`

**Pros:** Free forever, version control, professional
**Cons:** Requires GitHub knowledge

---

### **🎯 METHOD 3: Vercel (FREE)**

**Similar to Netlify**

1. **Go to:** https://vercel.com
2. **Sign up** (free)
3. Click **"Add New"** → **"Project"**
4. **Import from GitHub** or **Upload folder**
5. Click **"Deploy"**
6. Get live URL: `your-site.vercel.app`

**Pros:** Fast, free, custom domains
**Cons:** Requires account

---

### **🎯 METHOD 4: Render (FREE)**

1. Go to: https://render.com
2. Sign up (free)
3. Click **"New"** → **"Static Site"**
4. Connect GitHub repo or upload
5. Deploy!

---

## 📁 **Git/GitHub Full Guide**

### **Installing Git**

**Windows:**
- Download: https://git-scm.com/download/win
- Install with default settings

**Mac:**
```bash
brew install git
```

**Linux:**
```bash
sudo apt install git
```

### **Upload to GitHub (Detailed)**

#### **Step 1: Initialize Git**
```bash
cd path/to/gradecalc
git init
```

#### **Step 2: Add Files**
```bash
git add .
git status  # Check what will be committed
```

#### **Step 3: Commit**
```bash
git commit -m "Initial commit - GradeCalc website"
```

#### **Step 4: Create GitHub Repo**
1. Go to https://github.com/new
2. Name: `gradecalc`
3. Don't initialize with README
4. Click "Create repository"

#### **Step 5: Push to GitHub**
```bash
# Replace 'yourusername' with your GitHub username
git remote add origin https://github.com/yourusername/gradecalc.git
git branch -M main
git push -u origin main
```

#### **Step 6: Update Later**
```bash
# After making changes
git add .
git commit -m "Updated features"
git push
```

---

## 🔧 **Troubleshooting**

### **Issue: Pages won't navigate locally**

**Solution:**
- Don't open HTML files directly (double-click)
- MUST use a local server (Python, VS Code Live Server, etc.)
- Or deploy online immediately

### **Issue: "index-complete.html not found"**

**Solution:**
```bash
# Rename the file
mv index-complete.html index.html
```

Or manually rename in your file explorer.

### **Issue: CSS/JS not loading**

**Check:**
- All files in same folder?
- No spaces in folder names?
- Using a server (not file://)

### **Issue: Git push fails**

**Solution:**
```bash
# Set up credentials
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Try pushing again
git push -u origin main
```

---

## 📊 **File Structure (Final)**

```
gradecalc/
├── index.html              ← Main GPA Calculator (START HERE)
├── cgpa.html               ← CGPA Tracker
├── goals.html              ← Academic Goals
├── analytics.html          ← Analytics Dashboard
├── guides.html             ← Grading Guides
├── about.html              ← About SME
└── README.md               ← Optional documentation
```

---

## ✅ **Deployment Checklist**

Before deploying:

- [ ] All 6 HTML files in one folder
- [ ] `index.html` exists (not index-complete.html)
- [ ] Tested locally with server
- [ ] All navigation links work
- [ ] Chose deployment platform (Netlify/GitHub/Vercel)
- [ ] Created account on platform
- [ ] Deployed successfully
- [ ] Tested live site
- [ ] Shared URL with users

---

## 🎯 **Recommended Workflow**

### **For Absolute Beginners:**
1. ✅ Use **Netlify Drop**
2. Drag folder → Get URL
3. Share with users
4. Total time: 2 minutes

### **For Developers:**
1. Upload to **GitHub**
2. Enable **GitHub Pages**
3. Use Git for version control
4. Total time: 5 minutes

### **For Production:**
1. Upload to **GitHub**
2. Connect to **Netlify/Vercel**
3. Auto-deploy on every commit
4. Add custom domain

---

## 🌟 **After Deployment**

### **Share Your Site:**
- Social media
- Email signature
- Student forums
- University groups

### **Monitor:**
- Check if pages load
- Test on mobile
- Test all features

### **Update:**
```bash
# Make changes locally
# Test changes
git add .
git commit -m "Updated X feature"
git push
# Auto-deploys if connected to Netlify/Vercel
```

---

## 💡 **Pro Tips**

1. **Custom Domain:**
   - Buy domain: Namecheap, Google Domains ($10-15/year)
   - Connect to Netlify/Vercel (free SSL included)

2. **Analytics (Optional):**
   - Add Google Analytics
   - Track visitors
   - See popular pages

3. **SEO:**
   - Add meta descriptions
   - Submit to Google Search Console
   - Create sitemap

4. **Performance:**
   - Already optimized (single-file pages)
   - No build step needed
   - Instant load times

---

## 🆘 **Need Help?**

### **Common Questions:**

**Q: Do I need a custom domain?**
A: No! Netlify/GitHub give free subdomains.

**Q: How much does hosting cost?**
A: $0. All platforms mentioned are FREE.

**Q: Can I update the site later?**
A: Yes! Just re-upload or push to Git.

**Q: Will it work on mobile?**
A: Yes! Fully responsive design.

**Q: Do I need a database?**
A: No! Everything runs in the browser.

---

## 🎉 **You're Ready!**

Your GradeCalc website is production-ready and can serve thousands of users immediately.

**Recommended Next Steps:**
1. Test locally (2 minutes)
2. Deploy to Netlify (2 minutes)
3. Share with students
4. Collect feedback
5. Update as needed

**Total Time to Live Website: 5 minutes**

---

## 📧 **Support**

If you encounter issues:
1. Check this guide first
2. Google the error message
3. Ask on Stack Overflow
4. GitHub Issues (if using GitHub)

---

**Good luck with your deployment! 🚀**

*Studies Made Easier - Empowering Students Worldwide*
