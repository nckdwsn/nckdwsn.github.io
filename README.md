# Nick Dawson — Professional Portfolio Site

Personal portfolio website hosted on GitHub Pages at [nckdwsn.github.io](https://nckdwsn.github.io).

## Site Structure

```
/
├── index.html          ← Main profile page (homepage)
├── experience.html     ← Full career timeline
├── speaking.html       ← Speaking engagements & video cards
├── projects.html       ← Strategic projects & initiatives
├── style.css           ← All styles (single shared stylesheet)
├── Nick_Dawson.jpg     ← Your profile photo
└── Nick_Dawson_CV_01_2026.pdf  ← CV download (add this file)
```

## How to Deploy to GitHub Pages

### Step 1 — Go to your repository
Open your browser and go to:
`https://github.com/nckdwsn/nckdwsn.github.io`

### Step 2 — Upload or replace files

**Option A: Via the GitHub web interface (easiest)**

1. Click **Add file → Upload files**
2. Drag and drop all the files from this folder:
   - `index.html`
   - `experience.html`
   - `speaking.html`
   - `projects.html`
   - `style.css`
   - `README.md`
   - `Nick_Dawson.jpg` (your photo)
   - `Nick_Dawson_CV_01_2026.pdf` (your CV — add this separately)
3. Scroll down, write a commit message such as `Redesign: dark theme portfolio`
4. Click **Commit changes**

Your site will be live at `https://nckdwsn.github.io` within 1–2 minutes.

**Option B: Via Git on your computer**

```bash
# Clone your repo (if you haven't already)
git clone https://github.com/nckdwsn/nckdwsn.github.io.git
cd nckdwsn.github.io

# Copy all new files into the folder, then:
git add .
git commit -m "Redesign: dark theme portfolio"
git push origin main
```

### Step 3 — Confirm your photo is named correctly
Your photo must be named exactly **`Nick_Dawson.jpg`** (capital N, capital D, .jpg extension) and placed in the root of your repository — the same folder as `index.html`. GitHub Pages is case-sensitive.

### Step 4 — Add your CV PDF (optional)
Place your CV file named **`Nick_Dawson_CV_01_2026.pdf`** in the root folder. The Download CV button will then work. If your file has a different name, update the `href` in `index.html`:
```html
<a href="YOUR_FILE_NAME.pdf" class="btn btn-primary" download>
```

---

## How to Add Speaking Videos

Open `speaking.html`. Each video card looks like this:

```html
<div class="card">
  <div class="card-thumb">
    <span class="card-thumb-label">Video placeholder</span>
    <span class="play-btn"><i class="ti ti-player-play"></i></span>
  </div>
  <div class="card-body">
    <p class="card-tag">MWC · Barcelona</p>
    <p class="card-title">Add your talk title here</p>
    <p class="card-desc">Add a short description.</p>
  </div>
</div>
```

**To embed a YouTube video**, replace the entire `<div class="card-thumb">` block with:

```html
<div class="card-thumb" style="height:auto; padding:0;">
  <iframe width="100%" height="200"
    src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
    frameborder="0" allowfullscreen>
  </iframe>
</div>
```

Replace `YOUR_VIDEO_ID` with the 11-character code from your YouTube URL.
For example: `https://www.youtube.com/watch?v=dQw4w9WgXcQ` → ID is `dQw4w9WgXcQ`

---

## How to Add More Projects

Open `projects.html` and copy-paste a card block:

```html
<div class="card">
  <div class="card-body" style="padding: 1.25rem;">
    <p class="card-tag">Company Name · Year</p>
    <p class="card-title" style="font-size:14px;">Project Title</p>
    <p class="card-desc">Description of the project, your role, and the outcome.</p>
    <div style="margin-top:10px;">
      <span class="badge">Key metric</span>
      <span class="badge">Another badge</span>
    </div>
  </div>
</div>
```

---

## Editing Content

All content is plain HTML — no build tools, no frameworks, no npm. Open any `.html` file in a text editor (Notepad, VS Code, TextEdit) and edit the text directly between the tags.

**To change a metric in the Dashboard:**
Find the `<div class="dash-card">` blocks in `index.html` and update the `<span class="dash-val">` value.

**To update contact details:**
Search for `nckdwsn@protonmail.com` or `+49 162` across all four HTML files and replace as needed.

**To add a new competency card:**
Copy a `<div class="comp-card">` block in `index.html` and update its icon, title, and body text. Icon names come from [tabler.io/icons](https://tabler.io/icons) — use the format `ti ti-icon-name`.

---

## Technical Notes

- No JavaScript frameworks or build tools required
- Fonts load from Google Fonts (requires internet connection)
- Icons from Tabler Icons CDN (requires internet connection)
- Fully responsive — works on mobile, tablet, and desktop
- GitHub Pages serves the site for free with no ads
