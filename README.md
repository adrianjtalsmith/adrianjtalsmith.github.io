# adrianjtalsmith.github.io — personal academic website

A plain, static website: three HTML pages, one stylesheet, a folder of PDFs.
There is no build step and nothing to install. Editing the site means editing
the HTML in a text editor and pushing to GitHub.

## Files

| File | What it is |
|---|---|
| `index.html` | About page: short bio, contact, research themes |
| `publications.html` | Publications list, newest first, with PDF and DOI links |
| `work-in-progress.html` | Drafts, current projects, the GraspingAI collaboration |
| `style.css` | All styling. Colours are set once in the `:root` block at the top |
| `papers/` | PDFs linked from the site |
| `assets/` | Images (currently one small portrait) |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Publishing (one-off)

1. On GitHub, open the repository → **Settings → Pages**.
2. Under *Build and deployment*, set **Source** to *Deploy from a branch*,
   choose the `main` branch and the `/ (root)` folder, and save.
3. After a minute the site is live at `https://adrianjtalsmith.github.io/website/`.
   If the repository is renamed to `adrianjtalsmith.github.io` the site is
   served at `https://adrianjtalsmith.github.io/` instead.

A custom domain can be added later on the same settings page.

## Everyday updates

**Add a publication.** Copy the PDF into `papers/` using a lower-case,
hyphenated file name (for example `alsmith-2027-title-words.pdf`). Open
`publications.html`, copy one of the existing `<li> … </li>` blocks, paste it
under the right year heading, and edit the title, venue, and links.

**Add or update a draft.** Same idea in `work-in-progress.html`. The Elizans
entry currently points at `papers/Elizans-draft.pdf`; drop the file there and
the link works.

**Change the bio or research descriptions.** Edit the paragraphs in
`index.html`. Each research theme is a `<div class="theme">` block.

**Then publish.** From the site folder:

```
git add -A
git commit -m "Add new paper"
git push
```

GitHub Pages rebuilds within a minute or two.

## Local copy

To get the site onto a computer for the first time:

```
cd ~/Documents/Claude/Projects
git clone https://github.com/adrianjtalsmith/website.git
```

To preview locally, open `index.html` in a browser; no server is needed.

## Still to do

- Replace `assets/adrian-alsmith.jpg` with a higher-resolution portrait
  (the current one is 160×160 px).
- Add PDFs for the entries that have none yet: "Distal touch and the
  sensational model" (2023), "Curved sixth fingers" (2022), the vestibular
  paper (2021), "What is the body schema?" (2020), and the Cognition paper
  (2020). Check the volume and page numbers of the vestibular paper.
- Decide whether publisher-version PDFs stay on the site or are swapped for
  accepted manuscripts.
