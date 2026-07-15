# 1TILE Kitchen & Bath - Website

A static site, ready to host for free on GitHub Pages.

## Files
- `index.html` - the page
- `style.css` - all styling
- `assets/` - put your photos here (see below)

## 1. Add your photos
Drop your images into the `assets` folder using these exact filenames
(or edit the `src` paths in `index.html` to match your own filenames):

- `hero.jpg` - large hero background photo (1600px wide or more recommended)
- `project-1.jpg` through `project-6.jpg` - gallery photos

## 2. Host it for free on GitHub Pages
1. Create a free GitHub account at github.com if you don't have one.
2. Create a new repository (e.g. `1tile-website`). Keep it **public** (required for free Pages hosting).
3. Upload all the files in this folder (`index.html`, `style.css`, and the `assets` folder) into that repository - either by dragging them into the GitHub web uploader, or with git:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/1tile-website.git
   git push -u origin main
   ```
4. In the repository, go to **Settings -> Pages**.
5. Under "Build and deployment", set **Source** to "Deploy from a branch", branch = `main`, folder = `/ (root)`. Save.
6. GitHub will give you a live URL like `https://YOUR-USERNAME.github.io/1tile-website/` within a minute or two.

## 3. Connect your own domain (1tile.ca) - optional
1. In **Settings -> Pages**, add `1tile.ca` (or `www.1tile.ca`) under "Custom domain".
2. At your domain registrar (wherever you bought 1tile.ca), add these DNS records:
   - For `www.1tile.ca`: a CNAME record pointing to `YOUR-USERNAME.github.io`
   - For the root `1tile.ca`: A records pointing to GitHub's IPs:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
3. DNS changes can take a few hours to fully propagate. GitHub will show a green checkmark in Settings -> Pages once it's verified, and you can enable "Enforce HTTPS" after that.

## Notes
- Phone number is currently set to `647-721-5006` (`tel:+16477215006`) in three places: header, hero, and the sticky mobile call bar. Update all three if it changes.
- The sticky "Call for a Free Quote" bar only appears on mobile screens (under 768px wide) - this is intentional, since it's aimed at Google Ads mobile traffic.
- Everything is plain HTML/CSS with no build step, so you can edit directly in GitHub's web editor if you don't want to install anything locally.
