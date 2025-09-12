# loven.github.io
Portfolio Site

Where to find the code

I placed the full HTML/CSS/JS file in the canvas text document titled IT-Portfolio-GitHubPages-index.html. Open that file to copy the complete index.html.

Quick deployment (GitHub Pages)

Create a new public GitHub repository (e.g. yourname.github.io if you want user/organization pages or any repo for project pages).

Add these files to the repo:

index.html (the file you have).

An assets/ folder with any images, GIFs, and PDFs referenced in the JSON (e.g. assets/Resume.pdf, assets/linux-console.gif, etc.).

Commit & push to GitHub.

For user pages: name repository your-github-username.github.io and GitHub will serve the site at https://your-github-username.github.io/.
For project pages: enable GitHub Pages in Settings → Pages (choose branch main and folder / (root)), and your site will appear at https://your-github-username.github.io/<repo>/.

Done — recruiters can visit the URL and view the single-page portfolio.

How to maintain & manage content (recommended workflow)

Content source: the page contains a JSON block (<script type="application/json" id="site-data">) used to render sections. To update:

Edit the sections array in that JSON (titles, bullets, tags, and media entries).

Add media files (images, GIFs, PDFs) into assets/ and update media.src with the path assets/filename.

For YouTube, set media.type to "youtube" and src to the embed URL (e.g. https://www.youtube.com/embed/<id>).

Keep each section concise: 2–4 bullets + 1 case-study PDF + 1 demo video ideally.

Version control: every change is a Git commit. Use meaningful commit messages like “Add Linux case study PDF” or “Update DevOps tags”.

Large files: if your PDFs/videos are large, use Git LFS or host large videos on YouTube/Vimeo and embed them.

Assets organization:

assets/Resume.pdf — one-click resume for recruiters.

assets/images/ — screenshots, GIFs.

assets/pdfs/ — case studies, postmortems.

SEO & discoverability:

Add meta description, canonical tags if needed.

Keep section titles keyword-friendly (e.g., “Site Reliability Engineering — SLOs & Incident Response”).

Access & privacy:

If some case studies are sensitive, do not upload them publicly — instead add sanitized summaries or require a sign-in (not recommended for a public GitHub Pages site).

Editing for non-technical users:

If you'd prefer not to edit HTML, maintain site-data.json in the repo root and modify the HTML to fetch /site-data.json (simple change). Then non-tech users can edit JSON directly via GitHub web UI.

Testing:

After edits, run the site locally (open index.html) or push to a branch and use GitHub Pages preview to confirm layout and embedded media work.

Accessibility & recruiter friendliness:

Keep bullets short, include dates (e.g., “2022–2024: Managed 200+ EC2 instances”).

Put the resume and email at top-right so recruiters can act fast.

Use clear project names and simple captions for media.

Optional improvements you might want later

Move inline JSON to site-data.json for easier editing.

Add a small CI workflow (GitHub Actions) to validate links/assets and build an optimized version.

Add analytics (Plausible or Google Analytics) to see recruiter behavior (which sections they open).

Add a printable/responsive resume HTML view and a downloadable PDF generated from it.

Add language/version toggles or badges for certifications (e.g., AWS Certified).
