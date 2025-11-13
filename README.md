# Pilot Offer Page — Firebase Hosting Deployment

This project is a static landing page. The repository is prepared for Firebase Hosting.

Steps to deploy locally and to Firebase Hosting:

1. Install Firebase CLI (if you haven't already):

   npm install -g firebase-tools

2. Login to Firebase:

   firebase login

3. Initialize hosting (only if you want to re-run init locally):

   firebase init hosting

   - When prompted, choose "Use an existing project" and select your project.
   - Set the public directory to `public`.
   - Configure as a single-page app? Choose `Yes` to rewrite all routes to `index.html` (recommended for SPAs).

4. Replace the placeholder project id in `.firebaserc` with your Firebase project id:

   {
     "projects": { "default": "YOUR_FIREBASE_PROJECT_ID" }
   }

5. Deploy to Firebase Hosting:

   npm run deploy

Local testing:

- Serve the `public/` folder locally with:

  npm run serve

CI / GitHub Actions (optional):

- You can add `FIREBASE_TOKEN` as a repository secret and enable automatic deploys on push to `main`. A sample workflow is included at `.github/workflows/firebase-hosting-deploy.yml`.

If you need help finding your Firebase project id or setting up CI, tell me and I can assist.
