# Liweeitax V11 Mega Unified

V11 is a consolidated evolution of V1–V10. It keeps the existing social modules, fixes the duplicate-script issue from the previous line of builds, adds concrete features such as polls, mentions, scheduled posts, notification preferences, hidden words, profile editing endpoints, overview analytics, and a 900-entry capability registry.

## Important
The `/api/features` catalog intentionally distinguishes `active` capabilities from `hook`/roadmap integration points. A hook is not claimed to be a fully implemented third-party integration.

## Render
Use `npm start`. The service binds to `0.0.0.0` and `PORT`. Set `SESSION_SECRET` in Render Environment Variables. If you need SQLite/uploads to survive restarts, configure `LIWEETAX_DATA_DIR` and `LIWEETAX_UPLOADS_DIR` under a Render persistent disk mount.
