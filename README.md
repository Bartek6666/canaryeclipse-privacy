# canaryeclipse-privacy

Public privacy policy for the **Canary Eclipse** Android app — partial solar eclipse, 12 August 2026, Canary Islands.

Served as a static page via GitHub Pages at <https://privacy.canaryeclipse.com>.

The URL is referenced from the Google Play Store listing (required field) and
from the in-app Privacy screen. The in-app screen renders the same content
natively from `src/i18n/locales/*.ts` — this repo is the public, crawlable
copy that lives outside the app source tree.

## Files

- `index.html` — single-page policy, 4 languages (EN / PL / ES / DE), EN
  default, language switcher persisted in `localStorage`.
- `CNAME` — GitHub Pages custom domain binding (`privacy.canaryeclipse.com`).

## Updating

When the policy changes:

1. Edit `index.html` (all four `<article lang="…">` blocks).
2. Bump the version + date in each article's `<p class="meta">` line.
3. Update the same content in the app: `src/i18n/locales/{pl,en,es,de}.ts`
   under the `privacy.*` keys, and the `version` / `date` arguments passed
   to `t('privacy.version', …)` / `t('privacy.lastUpdated', …)` in
   `src/screens/PrivacyPolicyScreen.tsx`.
4. Commit and push — GitHub Pages redeploys automatically.

Contact: <contact@canaryeclipse.com>
