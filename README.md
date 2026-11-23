# Oliver Parks website

Static website for [oliverparks.com](https://www.oliverparks.com): English pages in the root, German pages in `/de/`, images and fonts in `/assets/`. No build step: every file is ready to serve as-is.

## Pages

| English | German |
|---|---|
| `index.html` | `de/index.html` |
| `about.html` | `de/about.html` |
| `what-we-do.html` | `de/what-we-do.html` |
| `our-approach.html` | `de/our-approach.html` |
| `consultants.html` | `de/consultants.html` |
| `careers.html` | `de/careers.html` |
| `story-tom.html`, `story-tiffany.html`, `story-isabel.html` | same in `de/` |
| `blog.html` | `de/blog.html` |
| `success-stories.html` | (English only) |
| `contact.html` | `de/contact.html` |
| `privacy.html` | `de/privacy.html` |
| `anti-slavery.html` | `de/anti-slavery.html` |
| `impressum.html` | `de/impressum.html` |

## Publishing (recommended: Netlify, free)

1. Create a new GitHub repository (e.g. `oliverparks-website`) and upload the contents of this folder to it.
2. In [Netlify](https://app.netlify.com): **Add new site → Import from Git → GitHub**, pick the repository. Leave the build command empty and the publish directory as `.` (already set in `netlify.toml`).
3. In Netlify **Domain management**, add `www.oliverparks.com` and follow the DNS instructions (a CNAME record at your domain registrar, e.g. Namesco).
4. Every change pushed to the `main` branch goes live automatically.

### Forms
The contact and application forms use **Netlify Forms** (`data-netlify="true"`). After the first deploy, open **Forms** in Netlify, then **Form notifications → Add notification → Email** and send submissions to `info@oliverparks.com`. Submissions return visitors to the page with a thank-you message.

### Alternative: GitHub Pages
The site also works on GitHub Pages (**Settings → Pages → Deploy from branch → main / root**; `CNAME` sets the custom domain). GitHub Pages cannot process forms, so the forms would need a service such as Formspree, and `_redirects` / `netlify.toml` are ignored.

## Editing
Edit the HTML files directly, or keep making changes in the Claude design canvas and export a new version. Text is plain HTML; the page styles are in the `<style>` block at the top of each page.
