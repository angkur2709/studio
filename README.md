# STUDIO — GitHub Pages Website

This folder is a complete static website for **STUDIO**, ready to publish with GitHub Pages.

## Pages

- `index.html` — Home
- `research.html` — Research themes and current directions
- `people.html` — Group members
- `publications.html` — Publication list
- `facilities.html` — Experimental capabilities and instruments
- `contact.html` — Contact information
- `404.html` — Custom not-found page
- `assets/css/style.css` — Shared visual design
- `assets/js/main.js` — Mobile navigation and footer year

## Publish with GitHub Pages

1. Create a new GitHub repository, for example `studio`.
2. Upload **the contents of this folder** to the repository root. `index.html` must be at the top level.
3. In GitHub, go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose branch **main** and folder **/(root)**, then save.
6. GitHub will publish the site at a URL similar to `https://YOUR-USERNAME.github.io/studio/`.

## Use `studio.angkurjyoti.com`

Once the GitHub Pages version works:

1. In your DNS provider for `angkurjyoti.com`, add a **CNAME** record:
   - Host / Name: `studio`
   - Target: `YOUR-USERNAME.github.io`
2. In GitHub **Settings → Pages → Custom domain**, enter `studio.angkurjyoti.com`.
3. After GitHub verifies the domain, enable **Enforce HTTPS**.
4. Copy `CNAME.example` to a file named exactly `CNAME` in the repository root, or let GitHub create it automatically when you save the custom domain.

Do **not** rename `CNAME.example` until your DNS record is configured.

## Make future edits

### Text changes
Open the corresponding `.html` file and edit the text. Most page content is plain HTML and intentionally easy to find.

### Global visual changes
Edit `assets/css/style.css`. The colors are defined at the top:

```css
:root {
  --ink: #11100f;
  --paper: #f1eee7;
  --red: #ff5a47;
  --blue: #2d59ff;
  --acid: #d8ff4a;
}
```

### Add a person photo
1. Put the image in `assets/images/`, for example `saksham.jpg`.
2. In `people.html`, replace:

```html
<div class="person-photo">SS</div>
```

with:

```html
<div class="person-photo"><img src="assets/images/saksham.jpg" alt="Saksham Sharma"></div>
```

### Add a publication
Copy one `.pub` block in `publications.html` and edit the year, title and link.

### Add a research project
Copy one `<article class="project">...</article>` block in `index.html`, or add a new `research-block` in `research.html`.

## Local preview on a Mac

From Terminal inside this folder:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000` in Safari or Chrome.

## Suggested workflow

For small edits, edit directly on GitHub. For larger redesigns, clone the repository to your Mac, edit in VS Code, preview locally, then commit and push. Every push to `main` automatically republishes the GitHub Pages site.
