# Ares commercial diligence, V2 (HTML password-protected site)

The site is `index.html`, the customer deliverable V2 of 4 October 2026 (with the Monro term-sheet section). It replaces the deliverable of 30 September 2026, which stays deployable from the `V1` folder. ## Deploy

Either way, Vercel detects no framework. Leave Build Command and Output Directory empty (Framework Preset: Other).

**Vercel CLI** (from this folder):

    npx vercel        # first time: link or create the project
    npx vercel --prod

**GitHub**: push this folder to a private repository, then in Vercel choose Add New, then Project, then import that repository and Deploy.

To replace V1 on the project that already serves it, link this folder to that project when the CLI asks (or replace the repository's contents with this folder's) and deploy with `--prod`.

## Notes

- Search engines are told not to index the site (`X-Robots-Tag` header and `robots.txt`).
- The page loads its fonts from Google Fonts. Everything else is inside `index.html`.
- `middleware.js`, `package.json`, `package-lock.json`, `vercel.json`, `robots.txt` and `.gitignore` are identical to V1's.
