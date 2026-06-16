# Taylor Bentley — Portfolio Site

A static rebuild of your Wix portfolio (Home, About, Resume, Projects + 3 project
detail pages), ready to host for free on GitHub Pages with your own domain.

## Files

```
index.html              Home
about.html               About
resume.html               Resume
projects.html              Projects list
projects/thrift.html        Thrive on Thrift project detail
projects/chrome-extensions.html
projects/golf.html
css/style.css             All styling
```

## 1. Put it on GitHub

1. Go to github.com and create a new repository. Two naming options:
   - `yourusername.github.io` → your site is live at `https://yourusername.github.io` (no extra config)
   - any other name, e.g. `portfolio` → your site is live at `https://yourusername.github.io/portfolio`
2. Upload these files to the repo (drag-and-drop on github.com works fine for this many files, or use `git push` if you're comfortable with git).

## 2. Turn on GitHub Pages

1. In the repo, go to **Settings → Pages**.
2. Under **Branch**, select `main` and folder `/ (root)`, then **Save**.
3. Wait a minute or two — your URL will appear at the top of that page.

## 3. Connect your custom domain (the free part)

1. Buy a domain from any registrar (Namecheap, Cloudflare, Google Domains successor, etc.) — this step always costs ~$10–15/year regardless of host.
2. In **Settings → Pages → Custom domain**, type your domain and save. This creates a `CNAME` file in your repo automatically.
3. At your domain registrar, add these DNS records:
   - For a root domain (`example.com`): four `A` records pointing to
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - For a `www` subdomain: a `CNAME` record pointing to `yourusername.github.io`
4. Back in GitHub Pages settings, check **Enforce HTTPS** once it becomes available (can take a few hours after DNS updates).

## Note on images and the resume PDF

To get you up and running immediately, the screenshots and the resume PDF in
these pages still point to your original Wix-hosted files (urls containing
`wixstatic.com` and `filesusr.com`). They'll keep working as long as that Wix
site exists. When you have a few minutes, it's worth downloading those files
and re-uploading them into this repo (e.g. an `assets/` folder), then updating
the `src=`/`href=` paths to point to your own copies — that way the site is
fully independent of Wix.
