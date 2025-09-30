# Notification Preferences Form

A single-page, accessible notification preference center demonstrating:

- Accessible form structure (legend, labels, live regions, skip link)
- Tri-state master checkbox (select / deselect / indeterminate)
- LocalStorage persistence with versioned schema (`email_prefs_v3`)
- Optional email capture field
- Debounced auto-save + manual Save button (POST action fallback)
- Dark / light theme toggle (system preference aware)
- Bootstrap 5 styling with graceful degradation
- Toast feedback for save/reset events

## File Structure
```
frontend/
  emailsettings.html
README.md
```

## Running Locally
Just open `frontend/emailsettings.html` in any modern browser. No build step required.

## Persistence
Preferences (and optional email) are stored in `localStorage` under the key `email_prefs_v3`. Bumping the key isolates older incompatible schemas.

## Accessibility Highlights
- Indeterminate state for bulk selection
- `aria-live` regions for toast / count updates
- High-contrast theming and focus ring
- Keyboard-only friendly interactions

## Dark Mode
A theme toggle button persists choice. If no explicit selection is stored, the system `prefers-color-scheme` is respected.

## Customizing
Edit or add categories by modifying the checkbox list inside `#prefList`. If you change the data model meaningfully, bump the storage key.

## Deploying
You can host this statically (GitHub Pages, Netlify, Vercel, S3). For GitHub Pages:
1. Push this repo to GitHub.
2. Enable Pages in repository settings (root / main branch).
3. Access via the provided Pages URL when GitHub finishes publishing.

## License
MIT (add a LICENSE file if you need explicit terms).

## Future Ideas
- Export/import JSON settings
- Analytics panel (history of changes)
- Localization scaffolding
- Unit tests for state logic
