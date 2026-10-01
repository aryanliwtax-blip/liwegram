# Liweeitax V13 — stability/auth fix

V13 keeps the existing V12 feature set and focuses on stability fixes.

## Fixed
- Authenticated sections refresh `/api/me` before opening, so Settings/Profile/Chat/Saved/Notifications do not rely on stale client auth state.
- API requests explicitly include same-origin credentials and disable API caching.
- Login/Create Account verifies that the server session is actually established before closing the auth modal.
- Render session cookie has a dedicated stable name and logout clears the correct cookie.
- `/api/me` is marked `no-store` so stale auth responses are not reused.
- Service-worker cache bumped to V13 to avoid serving the old shell after deployment.
- Service worker never intercepts API, upload, or its own update request.

## Validation
- `node --check server.js` passed.
- Extracted frontend JavaScript `node --check` passed.
- No feature removals were intentionally made.

For Render, keep `SESSION_SECRET` as a persistent environment variable. For durable production data, use persistent storage/database as appropriate.
