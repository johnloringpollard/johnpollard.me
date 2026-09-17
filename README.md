# John Pollard

Personal website for [johnpollard.me](https://johnpollard.me).

## Editing and previewing

Edit `index.html` directly. The page uses plain HTML and CSS, with no build step or package dependencies.

Open `index.html` in a browser, or serve the project locally:

```sh
python3 -m http.server 8080 --bind 127.0.0.1
```

Then visit <http://127.0.0.1:8080>.

The portrait is in `assets/`: the page uses the optimized WebP, and the full-resolution PNG is available for reuse.

## Publishing

GitHub Pages publishes the root of the `main` branch. Commit and push changes to update the site:

```sh
git add index.html assets
git commit -m "Update personal site"
git push
```

`CNAME` sets the custom domain to `johnpollard.me`. `.nojekyll` tells Pages to serve the static files directly.

## Domain setup

In Namecheap, open Domain List → Manage → Advanced DNS for `johnpollard.me`. Replace the parking or URL redirect records for `@` and `www` with these records. Keep unrelated records, including email records.

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | johnloringpollard.github.io |

Use Automatic TTL. After DNS resolves to GitHub and the TLS certificate is ready, enable **Enforce HTTPS** in the repository's Settings → Pages.

Reference: [GitHub Pages custom domain setup](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).
