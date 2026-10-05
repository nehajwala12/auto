# Ares commercial diligence, V2 (password-protected site)

The site is `index.html`, the customer deliverable V2 of 4 October 2026 (with the Monro term-sheet section). It replaces the deliverable of 30 September 2026, which stays deployable from the `V1` folder. `middleware.js` asks for a password on every request before anything is served.

- Password: `AutoCare2026`
- Username: anything (the browser asks for both; leave the name blank or type any word)

## Deploy

Either way, Vercel detects no framework. Leave Build Command and Output Directory empty (Framework Preset: Other).

**Vercel CLI** (from this folder):

    npx vercel        # first time: link or create the project
    npx vercel --prod

**GitHub**: push this folder to a private repository, then in Vercel choose Add New, then Project, then import that repository and Deploy.

To replace V1 on the project that already serves it, link this folder to that project when the CLI asks (or replace the repository's contents with this folder's) and deploy with `--prod`.

## Change the password

In the Vercel project, go to Settings, then Environment Variables. Add `SITE_PASSWORD` with the new value and redeploy. Without it, the default in `middleware.js` (`AutoCare2026`) applies.

## Notes

- Search engines are told not to index the site (`X-Robots-Tag` header and `robots.txt`).
- The page loads its fonts from Google Fonts. Everything else is inside `index.html`.
- `middleware.js`, `package.json`, `package-lock.json`, `vercel.json`, `robots.txt` and `.gitignore` are identical to V1's.
