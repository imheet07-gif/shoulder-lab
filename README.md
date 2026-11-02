# Shoulder Lab

A shoulder physiotherapy learning dashboard, hosted on GitHub Pages. Separate from Mars Log.

- Six levels and 18 short lessons
- Nine attributed video demonstrations
- Four fictional clinical cases with decision feedback
- Knowledge checks, search and rehabilitation progression examples
- Supabase email/password accounts and cross-device progress

## Run locally

Run `python3 -m http.server 8766` in this folder and open http://localhost:8766.

## Authentication and progress

Uses the existing public Supabase project configuration from Mars. Only the publishable browser key is included. No service-role key is used. The auth session uses its own `shoulder-lab-auth-v1` storage key. Progress is stored under `shoulder_lab_progress_v1` in the signed-in user's own metadata, rather than in Mars's tracker tables. Do not use this editable learning progress as an authorization or credentialing signal.

Email/password signup follows the project's existing confirmation and email delivery configuration. Confirmation may redirect to the project's existing Mars Site URL; return to Shoulder Lab to sign in. No Supabase settings or Mars source files are changed by this project. Signup email delivery and an authenticated round-trip need testing with a real account. Guest learning remains available without login. The static learning content is public, not access-controlled.

Progress is merged with the local account-specific record when signing in. Concurrent edits from multiple devices are not transactionally merged; avoid simultaneous sessions if exact progress reconciliation matters.

## Clinical scope

Educational summaries and simulated cases, not individual medical advice. Includes original-source links. Content has not undergone independent clinical peer review. Video demonstrations remain hosted by their creators. Advanced module labels indicate learning sequence, not clinical certification.

No AI calls or patient records are included.
