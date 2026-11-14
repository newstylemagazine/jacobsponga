# Jacob Sponga

A one-page writing site, styled after New Style. Hosted free on GitHub Pages.

## Adding an article

1. In `articles/`, copy `first-article.html` and rename it (e.g. `my-essay.html`).
2. Change the `<title>`, the `story-title` line, and the text inside `story-body` (one `<p>…</p>` per paragraph).
3. In `index.html`, copy an `<article>` block, paste it at the top of the list, and point it at your new file:

```html
<article class="post-card">
    <a class="post-link" href="articles/my-essay.html">
        <div class="post-meta">
            <h3><i>My Essay</i></h3>
            <p class="post-date">December 2026</p>
        </div>
    </a>
</article>
```

Each entry shows the title in italics with the date underneath.

All of this can be done in the browser on github.com: open a file, click the pencil to edit, or use **Add file → Upload files**. The site updates about a minute after you commit.

## Connecting your domain

1. Repo **Settings → Pages → Custom domain**: enter `www.yourdomain.com` and save (this creates a `CNAME` file).
2. At your domain registrar, add DNS records:
   - `CNAME` record: `www` → `newstylemagazine.github.io`
   - `A` records for the bare domain (`@`): `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
3. Once the domain checks out, tick **Enforce HTTPS**.
