ANNUAL GOALS FY 2026–27 — WEBSITE PACKAGE

Upload the included files and image assets to the ROOT of your existing GitHub repository (same folder as index.html). Keep your existing foundry.html and maintenance.html.

New flow:
- index.html: five-card landing page
- management.html: Management login, then four read-only progress cards
- department-review.html: read-only detail view for the selected department

IMPORTANT FIREBASE SETUP STILL REQUIRED:
1. Firebase Authentication accounts are used. Management UID configured in these files: jQoHH8MYHtf8AB9SWjYNn1RJvCN2. Foundry UID remains in foundry.html.
2. Update Realtime Database Rules so the Management UID can READ departments/*/dashboard, while only each department's authorized UID can WRITE its own dashboard. Do not make the database public.
3. Maintenance/Quality/Heat Treatment login pages and editable dashboards still need their own authorized Firebase accounts and department HTML implementations. Their landing-card links are retained as maintenance.html, quality.html, and heat-treatment.html. This package does not fabricate missing department dashboards.
4. Firebase web config is client-side configuration, not a password. Never put service-account private keys in HTML.

After uploading, test management.html directly, sign in, then open each department review card. If a card reports permission denied, the Firebase Rules are not yet configured for Management read access.
