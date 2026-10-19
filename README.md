# JessePuricelli.github.io

My portfolio, styled like a lab notebook. Live at https://jessepuricelli.github.io

Plain HTML and CSS: no framework, no build step, no JavaScript. Edit a file, commit, and GitHub Pages publishes it in a minute or two.

## Where things are

| File | What it is |
|---|---|
| `index.html` | Landing page: intro, featured projects, about, contact |
| `projects.html` | Index of every project |
| `projects/example-entry.html` | Template for a single project write-up |
| `assets/css/style.css` | All styling. Colors and fonts are at the very top |
| `assets/img/` | Photos and images |
| `assets/fonts/` | Fonts, stored here so nothing loads from other sites |

## Common edits

**Add a project**
1. Copy `projects/example-entry.html`, rename it (e.g. `projects/audio-amp.html`) and fill it in.
2. In `projects.html`, copy one `<li>...</li>` block to the top of the list and point it at the new page.
3. To feature it on the landing page, copy a `<a class="card">...</a>` block in `index.html`.

**Add a photo:** put it in `assets/img/`, then replace a `<div class="photo-slot">...</div>` with
`<img src="assets/img/photo.jpg" alt="what the photo shows">` (use `../assets/img/...` inside the `projects/` folder).

**Change colors or fonts:** edit the variables in the first block of `assets/css/style.css`.

**Preview locally:** just open `index.html` in a browser.

## Safety checklist

This site is public, so before committing:

- [ ] **No secrets.** This site needs no API keys, passwords or tokens. If code from a project uses one, leave it out or replace it with `YOUR_KEY_HERE`. `.gitignore` blocks common secret files, but double check.
- [ ] **Strip photo location data.** Phone photos can contain GPS coordinates of where they were taken. Remove it before uploading (on Windows: right-click the file → Properties → Details → "Remove Properties and Personal Information"; on a Mac, export from Photos with "Include location" off).
- [ ] **Check documents and screenshots** for personal info: home address, phone number, student ID, other people's names.
- [ ] **Resume:** consider leaving your phone number and street address off the public version.
- [ ] **Commit email:** use GitHub's private address (Settings → Emails → "Keep my email addresses private") so your personal email isn't attached to commits.

Security built into the pages: a Content-Security-Policy blocks all scripts and anything loaded from other sites, external links use `rel="noopener noreferrer"`, and there are no trackers or analytics.
