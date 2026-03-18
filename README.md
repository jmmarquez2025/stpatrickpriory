# St. Patrick's Priory — stpatrickpriory.com

Website for the Dominican Priory at St. Patrick Church, Columbus, Ohio.

## Deploying to GitHub Pages

### 1. Create the GitHub repository
1. Go to [github.com/new](https://github.com/new)
2. Name it `stpatrickpriory` (or any name you like)
3. Set it to **Public**
4. Click **Create repository**

### 2. Push this code
```bash
cd stpatrickpriory
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/stpatrickpriory.git
git push -u origin main
```


### 3. Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose `main` branch, `/ (root)` folder
4. Click **Save**

### 4. Connect your custom domain
1. Still in **Settings → Pages**, enter `stpatrickpriory.com` under **Custom domain**
2. Click **Save**
3. Check **Enforce HTTPS** once it becomes available

### 5. Configure DNS at your domain registrar
Add these DNS records where you purchased `stpatrickpriory.com`:

**A Records** (point to GitHub Pages):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME Record** (for www subdomain):
```
www → YOUR_USERNAME.github.io
```

DNS changes can take up to 24–48 hours to propagate.

## Customizing the Site

### Replacing placeholder content
- **Images**: Replace the `<div class="img-placeholder">` elements with `<img>` tags
- **Friar names/roles**: Edit the `.friar-card` sections in `index.html`
- **Text**: All placeholder copy is in `index.html` — edit directly
- **Contact info**: Update address, phone, and email in the contact section
- **Logo**: Replace the text-based logo in `.nav-logo` and `.footer-logo` with an `<img>` tag

### Adding a favicon
Place a `favicon.ico` in the root folder and add to `<head>`:
```html
<link rel="icon" href="/favicon.ico">
```

## Tech Stack
- Pure HTML, CSS, JavaScript — no build step required
- Google Fonts (Cinzel, Cormorant Garamond, Source Sans 3)
- Scroll-reveal animations via Intersection Observer
- Fully responsive (mobile, tablet, desktop)
