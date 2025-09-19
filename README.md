# Logly Landing Page - Deployment Guide

## 🚀 Quick Deploy to Vercel

### Option 1: Deploy via Vercel Website (Easiest - 2 minutes)

1. **Go to Vercel**
   - Visit [vercel.com](https://vercel.com)
   - Click "Sign Up" (use GitHub, GitLab, or email)
   - If you already have an account, click "Log In"

2. **Deploy Your Website**
   - Click the "Add New..." button → Select "Project"
   - Choose "Deploy from Local" (or drag & drop option)
   - Drag the entire `logly-website` folder onto the upload area
   - OR click "Select Folder" and choose the `logly-website` folder

3. **Configure Project**
   - Project Name: `logly-website` (or leave default)
   - Framework Preset: Select "Other" (it's just HTML/CSS/JS)
   - Click "Deploy"

4. **Wait for Deployment**
   - Takes about 30 seconds
   - You'll get a temporary URL like: `logly-website-abc123.vercel.app`
   - Click the URL to see your live website!

### Option 2: Deploy via Command Line

If you prefer using the terminal:

```bash
# Install Vercel CLI
npm i -g vercel

# Navigate to your website folder
cd /Users/brian/Projects/Logly/logly-website

# Deploy
vercel

# Follow the prompts:
# - Set up and deploy? Y
# - Which scope? (select your account)
# - Link to existing project? N
# - Project name? logly-website
# - Directory? ./ (current directory)
# - Want to override settings? N
```

## 🌐 Connect Your Domain (logly.app)

### Step 1: Add Domain to Vercel

1. **In Vercel Dashboard**
   - Go to your project (logly-website)
   - Click "Settings" tab
   - Click "Domains" in the left sidebar
   - Enter `logly.app` and click "Add"

2. **Vercel will show you DNS records**
   - You'll see something like:
     - Type: A, Name: @, Value: 76.76.21.21
     - Type: CNAME, Name: www, Value: cname.vercel-dns.com

### Step 2: Configure GoDaddy DNS

1. **Log into GoDaddy**
   - Go to [godaddy.com](https://godaddy.com)
   - My Products → Domains → Click "Manage" next to logly.app

2. **Update DNS Settings**
   - Click "DNS" or "Manage DNS"
   - Delete any existing A or CNAME records for @ and www

3. **Add Vercel Records**

   **For the root domain (logly.app):**
   - Click "Add Record"
   - Type: `A`
   - Name: `@`
   - Value: `76.76.21.21` (use the IP from Vercel)
   - TTL: 1 Hour

   **For www subdomain (www.logly.app):**
   - Click "Add Record"
   - Type: `CNAME`
   - Name: `www`
   - Value: `cname.vercel-dns.com` (use value from Vercel)
   - TTL: 1 Hour

4. **Save Changes**
   - Click "Save" in GoDaddy
   - DNS propagation takes 5-60 minutes

### Step 3: Verify in Vercel

1. Go back to Vercel project → Settings → Domains
2. You'll see "Valid Configuration" ✅ when DNS is working
3. Your website is now live at `logly.app`!

## 📝 Updating Your Website

### Quick Updates

1. **Edit files locally** in the `logly-website` folder
2. **Redeploy to Vercel:**

   **Option A: Drag & Drop**
   - Go to your project in Vercel dashboard
   - Click "Deployments" tab
   - Drag the updated folder to upload area

   **Option B: Command Line**
   ```bash
   cd /Users/brian/Projects/Logly/logly-website
   vercel --prod
   ```

### Automatic Updates (Advanced)

Push to GitHub and connect Vercel for auto-deploy:

1. Push website to GitHub repository
2. In Vercel: Import Git Repository
3. Every push to GitHub auto-deploys

## 🎨 Customization Tips

### Things to Update:

1. **App Store Link** (index.html)
   - Find: `href="#"`
   - Replace with: `href="https://apps.apple.com/app/your-app-id"`

2. **Email Contact** (index.html)
   - Find: `support@logly.app`
   - Replace with your actual email

3. **Privacy & Terms Links** (index.html)
   - Add actual URLs when you have these pages

4. **Colors** (styles.css)
   ```css
   :root {
       --primary-color: #007AFF;  /* Change to your brand color */
       --gradient-1: /* Your gradient */
   }
   ```

5. **Content** (index.html)
   - Update headlines, descriptions
   - Add real app screenshots
   - Include testimonials when available

## 🔧 Troubleshooting

### Domain not working?
- Wait up to 1 hour for DNS propagation
- Clear browser cache
- Try in incognito/private mode
- Check DNS with: `nslookup logly.app`

### Changes not showing?
- Hard refresh: Cmd+Shift+R (Mac) or Ctrl+Shift+R (Windows)
- Vercel caches for 5 minutes, wait or purge cache in dashboard

### Need SSL/HTTPS?
- Vercel provides free SSL automatically
- No configuration needed

## 📱 Testing

### Desktop
- Chrome, Safari, Firefox, Edge
- Resize window to test responsiveness

### Mobile
- Open on your phone: `logly.app`
- Test both portrait and landscape
- Check all buttons and links work

## 🎉 You're Done!

Your website should now be live at:
- `logly.app`
- `www.logly.app`
- Your Vercel URL (backup)

## Need Help?

- Vercel Docs: [vercel.com/docs](https://vercel.com/docs)
- GoDaddy Support: DNS settings help
- Common issues covered above

---

**Last Updated**: January 2025
**Created for**: Logly iOS App Landing Page