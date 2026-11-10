# caloreai.app

The public pages for **Calore**, the meal-scanning nutrition app.

```
privacy/          caloreai.app/privacy
delete-account/   caloreai.app/delete-account
```

Both stores require a privacy policy URL, and Google Play specifically
requires an account-deletion page reachable without installing the app.

## Why this is a separate repository

The app itself is private. GitHub Pages only serves public repositories on
the free plan, so the two pages live here — three files that say nothing
about how the app works — rather than making the whole product public to
host them.

Static HTML with no build step. Edit a file, push, and the site updates.

## Local preview

```bash
python3 -m http.server 4321
```

Then open `http://localhost:4321/privacy/`. Serve it rather than opening the
files directly: the relative stylesheet and the links between the pages only
resolve over HTTP.
