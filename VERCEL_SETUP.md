# 🚀 Connect GitHub to Vercel - Auto-Deploy Setup

## ✅ What's Already Done
- ✓ Git repository initialized
- ✓ GitHub repository created: https://github.com/bmartindev/logly-website
- ✓ All files pushed to GitHub

## 🔗 Now Connect to Vercel (2 minutes)

### Step 1: Go to Vercel
1. Visit [vercel.com](https://vercel.com)
2. Log in to your account

### Step 2: Import GitHub Repository
1. Click **"Add New..."** → **"Project"**
2. Select **"Import Git Repository"**
3. If asked, **authorize GitHub access**:
   - Click "Install" or "Configure"
   - Select your GitHub account
   - Choose "All repositories" or just select "logly-website"

### Step 3: Select Your Repository
1. Find **`logly-website`** in the list
2. Click **"Import"**

### Step 4: Configure Project
- **Project Name**: `logly-website` (or leave default)
- **Framework Preset**: Select **"Other"**
- **Root Directory**: `.` (leave as is)
- **Build Settings**: Leave all empty (no build needed)
- Click **"Deploy"**

### Step 5: Add Your Domain
After deployment (takes ~30 seconds):
1. Click **"Go to Dashboard"**
2. Go to **"Settings"** → **"Domains"**
3. Add **`logly.app`**
4. Follow the DNS instructions (same as before in GoDaddy)

## 🎉 You're Now Set Up!

### What This Means:
- ✅ **Automatic deploys**: Every push to GitHub triggers a new deployment
- ✅ **Edit anywhere**: Make changes from any computer
- ✅ **Version history**: All changes tracked in Git
- ✅ **Instant updates**: Changes go live in ~45 seconds

## 📝 How to Update Your Website Now

### From Your Mac (Primary Computer):
```bash
# 1. Make your changes to any files
# 2. Save changes
# 3. Push to GitHub:
cd /Users/brian/Projects/Logly/logly-website
git add .
git commit -m "Update: description of changes"
git push

# That's it! Vercel auto-deploys in ~45 seconds
```

### From Another Computer:
```bash
# 1. Clone the repository
git clone https://github.com/bmartindev/logly-website.git
cd logly-website

# 2. Make changes to files
# 3. Push changes
git add .
git commit -m "Update: description of changes"
git push

# Auto-deploys!
```

### From GitHub Web (Quick Edits):
1. Go to https://github.com/bmartindev/logly-website
2. Click any file → Click pencil icon to edit
3. Make changes
4. Click "Commit changes"
5. Auto-deploys!

### From Your Phone:
1. Download GitHub mobile app
2. Open your repository
3. Edit files directly
4. Commit changes
5. Auto-deploys!

## 🔧 Common Tasks

### Check Deployment Status:
- Vercel Dashboard → Your project → "Deployments" tab
- Green checkmark = Live
- Building = In progress (~45 seconds)

### View Live Site:
- Production: https://logly.app (once DNS is set up)
- Vercel URL: Check dashboard for .vercel.app link
- GitHub: Click "Environments" → "Production" → "View deployment"

### Rollback Changes:
1. Vercel Dashboard → "Deployments"
2. Find previous good deployment
3. Click "..." → "Promote to Production"

## 💡 Pro Tips

### Quick Content Updates:
Edit these in `index.html`:
- Hero title/subtitle
- Feature descriptions
- App Store links
- Contact info

### Style Changes:
Edit `styles.css`:
- Colors in `:root` section
- Fonts
- Spacing

### Add Analytics:
1. Edit `index.html`
2. Add analytics script before `</head>`
3. Commit & push
4. Auto-deploys with analytics

## 🆘 Troubleshooting

**Changes not showing?**
- Check Vercel dashboard for deployment status
- Clear browser cache (Cmd+Shift+R)
- Check GitHub: did the push succeed?

**Build failed?**
- Check Vercel dashboard for error message
- Usually it's a typo in HTML/CSS
- Fix locally, push again

**Need to change GitHub repo?**
- Vercel Settings → Git → Disconnect
- Connect new repository

## 📱 Your Website URLs

- **GitHub Repository**: https://github.com/bmartindev/logly-website
- **Production Domain**: https://logly.app (after DNS setup)
- **Vercel Dashboard**: Visit vercel.com → Your projects

---

You're all set! Every change you push to GitHub will automatically deploy to your live website. No more manual dragging and dropping! 🎉