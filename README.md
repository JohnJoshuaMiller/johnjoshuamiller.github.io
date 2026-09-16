# Simple Personal Website

A dependency-free personal website for GitHub Pages. It uses plain HTML and one small CSS file. There is no JavaScript, build system, package manager, framework, or database.

## Structure

```text
personal-site/
├── index.html
├── updates.html
├── thoughts.html
├── poetry.html
├── style.css
├── .nojekyll
└── essays/
    └── example-essay.html
```

- `index.html`: homepage
- `updates.html`: one scrolling page of personal/professional updates
- `thoughts.html`: index of essays, with each longer essay linked as its own page
- `poetry.html`: one scrolling page of poems
- `essays/`: standalone essay HTML files
- `style.css`: minimal styling shared across all pages
- `.nojekyll`: tells GitHub Pages to serve the files as a plain static site without Jekyll processing

## Before publishing

Search the files for `Your Name` and replace it with your actual name. Also edit the homepage bio and delete or replace the example content.

## Add an update

Open `updates.html` and copy an existing `<section class="entry">...</section>` block. Put the newest update at the top.

## Add a poem

Open `poetry.html` and copy an existing `<article class="entry">...</article>` block. The `poem` class preserves line breaks, so you can type the poem naturally inside the paragraph.

## Add an essay

1. Copy `essays/example-essay.html` to a new filename such as `essays/on-statistics.html`.
2. Change its `<title>`, `<h1>`, date, description, and body text.
3. Add a link to the new essay in `thoughts.html`.

Example:

```html
<li>
  <a href="essays/on-statistics.html"><strong>On Statistics</strong></a><br>
  <span class="meta">October 2026 — A short description.</span>
</li>
```

Use lowercase filenames with hyphens and no spaces when possible.

## Publish with GitHub Pages

### Option A: personal root site

Create a repository named exactly:

```text
YOUR-GITHUB-USERNAME.github.io
```

Put these files at the repository root and push them to the `main` branch. Your site will use the root URL:

```text
https://YOUR-GITHUB-USERNAME.github.io/
```

### Option B: project repository

You can instead use a repository with any name, for example `personal-site`. Its default URL will look like:

```text
https://YOUR-GITHUB-USERNAME.github.io/personal-site/
```

Because all links in this template are relative, both approaches work without modification.

### GitHub Pages settings

In the repository on GitHub:

1. Open **Settings**.
2. Open **Pages** in the sidebar.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and `/ (root)` folder.
5. Save.

GitHub will publish the site after the Pages deployment completes.

## Typical editing workflow

```bash
git clone https://github.com/YOUR-GITHUB-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY

# edit files

git add .
git commit -m "Update website"
git push
```

Every push to the configured publishing branch updates the site.

## Preview locally

For a site this simple, you can usually double-click `index.html` and open it directly in your browser.

If you prefer to serve it locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Keeping it simple

You do not need Jekyll, Hugo, React, Node, npm, or a CMS for this structure. New content is just new or edited HTML.
