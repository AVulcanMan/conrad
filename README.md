# conrad
anjali and vedant like little kids

# NimbusPower - Innovation Stage Website

A static website showcasing NimbusPower: a rechargeable sodium-ion pouch battery for eVTOLs with integrated passive thermal cooling coating.

**Tagline:** Fly safer, lift higher, powered by NimbusPower.

## 🚀 Quick Start

### Preview Locally

1. **Option 1: Simple File Opening**
   - Simply open `index.html` in your web browser
   - All assets are linked relatively and will load correctly

2. **Option 2: Local Server (Recommended)**
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Python 2
   python -m SimpleHTTPServer 8000
   
   # Using Node.js (if you have http-server installed)
   npx http-server
   ```
   - Then open `http://localhost:8000` in your browser

3. **Using VS Code Live Server**
   - Install the "Live Server" extension
   - Right-click on `index.html` and select "Open with Live Server"

## 📁 Project Structure

```
conrad/
├── index.html              # Main HTML file
├── assets/
│   ├── styles.css         # All styles
│   └── main.js            # JavaScript functionality
├── README.md              # This file
└── docs/                  # (Optional) For GitHub Pages deployment
```

## 🌐 Deployment to GitHub Pages

### Method 1: Deploy from Root Directory

1. **Push your files to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: NimbusPower website"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

2. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages**
   - Under "Source", select **Deploy from a branch**
   - Choose branch: **main** (or **master**)
   - Choose folder: **/ (root)**
   - Click **Save**

3. **Access your site**
   - Your site will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO/`
   - It may take a few minutes to go live

### Method 2: Deploy from `/docs` Folder

1. **Create a `docs` folder** (if it doesn't exist)
   ```bash
   mkdir docs
   ```

2. **Copy files to `docs` folder**
   ```bash
   # On Windows (PowerShell)
   Copy-Item index.html docs/
   Copy-Item -Recurse assets docs/
   
   # On Mac/Linux
   cp index.html docs/
   cp -r assets docs/
   ```

3. **Update paths in `docs/index.html`** (if needed)
   - The paths should already be relative (`assets/styles.css`), so they should work as-is
   - If you encounter issues, ensure paths start with `./` or are relative

4. **Push to GitHub**
   ```bash
   git add docs/
   git commit -m "Add docs folder for GitHub Pages"
   git push
   ```

5. **Enable GitHub Pages**
   - Go to **Settings** → **Pages**
   - Under "Source", select **Deploy from a branch**
   - Choose branch: **main** (or **master**)
   - Choose folder: **/docs**
   - Click **Save**

## 🔧 Custom Domain Setup (Optional)

1. **Add a `CNAME` file** to your repository root (or `docs/` folder if using that method)
   ```
   yourdomain.com
   www.yourdomain.com
   ```

2. **Configure DNS** at your domain provider:
   - Add a `CNAME` record pointing `www` to `YOUR_USERNAME.github.io`
   - Add an `A` record pointing the root domain to GitHub's IP addresses:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153

3. **Update GitHub Pages settings**
   - In **Settings** → **Pages**, enter your custom domain
   - Check "Enforce HTTPS" (available after DNS propagates)

## 📝 Replacing Placeholders

### 1. Innovation Brief PDF

Replace the placeholder PDF link:
- **File location:** `assets/innovation-brief.pdf`
- **In `index.html`:** Update the href in the "View Innovation Brief" button
  ```html
  <a href="assets/innovation-brief.pdf" class="btn btn-primary" target="_blank">
  ```

### 2. Innovation Video

Replace the video placeholder:
- **Option 1: YouTube**
  ```html
  <a href="https://www.youtube.com/watch?v=YOUR_VIDEO_ID" class="btn btn-secondary">
  ```

- **Option 2: Vimeo**
  ```html
  <a href="https://vimeo.com/YOUR_VIDEO_ID" class="btn btn-secondary">
  ```

- **Option 3: Embedded Video**
  Replace the button with an embedded iframe:
  ```html
  <div class="video-container">
    <iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" frameborder="0" allowfullscreen></iframe>
  </div>
  ```

### 3. Contact Information

Update the contact placeholder in the footer section:
- **Location:** Footer section in `index.html`
- **Replace:**
  ```html
  <p class="contact-placeholder">[Contact email placeholder]</p>
  ```
  With:
  ```html
  <p><a href="mailto:contact@nimbuspower.com">contact@nimbuspower.com</a></p>
  ```

## 🎨 Customization

### Colors

Edit CSS variables in `assets/styles.css`:
```css
:root {
    --primary: #4a9eff;
    --secondary: #ff6b9d;
    --accent: #4ecdc4;
    /* ... */
}
```

### Content

All content is in `index.html`. Edit sections directly:
- Hero section: Update title, tagline, description
- Quick Facts: Modify numbers and labels
- Sections: Update text, lists, and details

### Diagrams

SVG diagrams are inline in the Technology section. Edit them directly in `index.html` or replace with external SVG files.

## ✅ Features

- ✅ Fully responsive design (mobile, tablet, desktop)
- ✅ Accessible (WCAG guidelines, keyboard navigation, focus styles)
- ✅ Fast loading (no external dependencies except Google Fonts)
- ✅ SEO-friendly (meta tags, semantic HTML)
- ✅ Dark mode aerospace theme
- ✅ Smooth scrolling navigation
- ✅ Interactive accordions
- ✅ Animated elements on scroll
- ✅ Mobile-friendly hamburger menu

## 🔍 Testing Checklist

Before deploying, verify:

- [ ] All links work correctly
- [ ] Images/diagrams display properly
- [ ] Mobile menu functions correctly
- [ ] Smooth scrolling works
- [ ] Accordions expand/collapse
- [ ] All sections are accessible
- [ ] Footer contact placeholder is updated (or removed)
- [ ] PDF and video links are updated
- [ ] Site works when opened directly as `index.html`
- [ ] Site works when served from a local server
- [ ] Site works on GitHub Pages

## 📊 Performance

The site is optimized for:
- **Lighthouse Performance:** 90+ (expected)
- **Accessibility:** 100 (expected)
- **Best Practices:** 100 (expected)
- **SEO:** 100 (expected)

Optimizations include:
- Minimal external dependencies
- Inline SVG diagrams (no image requests)
- Efficient CSS (no unused styles)
- Lazy loading support
- Optimized fonts (Google Fonts with display=swap)

## 🐛 Troubleshooting

### Images/Assets Not Loading
- Ensure file paths are correct (case-sensitive on some servers)
- Check that `assets/` folder exists and contains all files
- Verify paths are relative (start with `assets/` not `/assets/`)

### GitHub Pages Not Updating
- Wait 5-10 minutes for changes to propagate
- Clear browser cache
- Check GitHub Actions tab for build errors
- Verify branch and folder settings in Pages settings

### Mobile Menu Not Working
- Ensure `main.js` is loaded correctly
- Check browser console for JavaScript errors
- Verify HTML structure matches JavaScript selectors

### Styles Not Applying
- Check that `styles.css` path is correct
- Verify CSS file is in `assets/` folder
- Clear browser cache

## 📄 License

This is a concept project for Conrad Challenge Innovation Stage.

## 👥 Team

- **Vedant P.** - Project Lead & Battery Design Specialist
- **Anjali P.** - System Modeling & Digital Prototyping Specialist
- **Yashas P.** - Thermal Materials / Coating Chemistry Specialist
- **Manya V.** - Business Strategy & Website Development

---

**Built with:** HTML5, CSS3, Vanilla JavaScript  
**No build step required** - Just open and go!
