# LabTrack v36 TEST — isolated starter (not production-ready)

This is a **safe staging scaffold** extracted from the v35 application. It is not yet the completed performance-optimized v36. It deliberately blocks the production Firebase project `labtrack-c55fb`.

## Setup
1. Create a NEW Firebase project with `test` in its project ID, on the Spark (free) plan. Do not link billing.
2. Enable Email/Password Authentication and create the same instructor email addresses as separate accounts. Passwords cannot be copied from production.
3. Create Firestore and configure security rules reviewed for the TEST project. The app's setup screen displays inherited v35 rules, which require a security review before importing real data.
4. Create a NEW GitHub repository (public if using GitHub Pages on GitHub Free). Upload `index.html` and the `assets/` folder, then enable GitHub Pages from the root of the main branch.
5. Open the TEST URL and paste the TEST project's Firebase web configuration. The app rejects production's project ID and rejects project IDs without `test`, `stage`, `dev`, or `sandbox`.

## Important limits
- This starter preserves the existing v35 functionality while separating CSS and JavaScript. It is **not yet a fully modular architecture**, and optimization, stress tests, JSON restore, and concurrent edit tests remain to be implemented.
- **Do not commit real student JSON backups or instructor passwords to GitHub.**
- The uploaded JSON has `config`, `labs`, and `students` arrays; do not assume it includes Firebase Authentication users or all auxiliary collections.
- Do not use real student data in a public test environment until access rules and permissions have been reviewed. Use synthetic records first.
- GitHub Pages requires HTTP(S); do not open the file directly as `file://`.
- This package makes no changes to production.
