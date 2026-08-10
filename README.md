# Pei Zhou Personal Homepage

Static, self-contained, GitHub Pages-ready personal homepage.

All resources needed to render the page are stored in this directory. External
URLs are used only as destinations for paper, project, code, and email links.

## Local Preview

From this folder:

```bash
python3 -m http.server 8000
```

Then open:

```
http://localhost:8000
```

The site has no build step. It can also be opened directly from `index.html`, but the local server path is closer to GitHub Pages behavior.

## Publish as PeiZhou26.github.io

Create a public GitHub repository named exactly:

```
PeiZhou26.github.io
```

The contents of this directory, not the enclosing `homepage` directory itself,
must be placed at the repository root. In the published repository,
`index.html` should therefore appear at:

```
PeiZhou26.github.io/index.html
```

One safe workflow is to clone the new repository elsewhere, copy this
directory's contents into it, and push:

```bash
cd /Users/peizhou/Desktop
git clone https://github.com/PeiZhou26/PeiZhou26.github.io.git
cp -R /Users/peizhou/Desktop/overleaf/Pei_Zhou_CV/homepage/. PeiZhou26.github.io/
cd PeiZhou26.github.io
git add .
git commit -m "Publish personal homepage"
git branch -M main
git push -u origin main
```

Then open the repository on GitHub and select:

```
Settings -> Pages -> Build and deployment
Source: Deploy from a branch
Branch: main
Folder: /(root)
```

The public URL will be:

```
https://peizhou26.github.io/
```

## Assets

- `assets/hero-wide.jpg`: optimized desktop hero image.
- `assets/hero-mobile.jpg`: optimized mobile hero image.
- `assets/publications/`: local publication overview and teaser images.
- `.nojekyll`: tells GitHub Pages to serve the static files directly.
