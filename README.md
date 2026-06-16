# Fix for tabentley1-afk.github.io

## What went wrong
When the files were uploaded, GitHub's drag-and-drop uploader flattened the
folder structure — `css/style.css` and the `projects/` pages ended up sitting
directly in the repo root instead of inside subfolders. So `index.html` was
looking for `css/style.css` (404) and pages were unstyled, and links to
project pages were pointing at paths that didn't exist.

## The fix
These files are flat on purpose — no subfolders — matching exactly what's
already in your repo:

```
index.html
about.html
resume.html
projects.html
thrift.html
chrome-extensions.html
golf.html
style.css
```

## How to apply it
1. Go to your repo on github.com (`tabentley1-afk/tabentley1-afk.github.io`).
2. Click **Add file → Upload files**.
3. Drag in all 8 files from this folder. Since the filenames match what's
   already there, GitHub will ask to replace the existing versions — confirm.
4. Commit directly to `main`.
5. Give it ~30–60 seconds, then refresh `https://tabentley1-afk.github.io/`
   (hard refresh / clear cache if it still looks unstyled).

That's it — no folders to recreate, no settings to change.

## About the resume PDF and images
These still point to your original Wix-hosted files. They'll keep working
as long as that Wix site exists. Re-hosting them in this repo later is a
nice-to-have, not required for the site to work.
