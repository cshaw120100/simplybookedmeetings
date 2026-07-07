# Simply Booked Meetings

A public, static landing page that can be deployed directly to Vercel.

## Project Structure

```text
simplybookedmeetings/
  index.html
  src/
    styles.css
    main.js
  public/
    favicon.svg
  vercel.json
  package.json
```

## Local Preview

From this folder:

```bash
npm install
npm run dev
```

Then open:

```text
http://127.0.0.1:5173
```

## Customize Before Launch

1. Replace the form email in `index.html` with your real address, or swap the form for your CRM/form provider.
2. Update service copy, result numbers, and the Unsplash hero image if you want a more specific brand direction.
3. Keep `vercel.json` at the project root so Vercel uses clean URLs.

## Connect to GitHub

1. Create a new repository on GitHub.
2. From this folder, initialize Git:

```bash
git init
git add .
git commit -m "Add agency landing page"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

If this will live inside a larger app repository later, put this landing page at the app root or in a dedicated folder such as `apps/marketing`, then select that folder as the Vercel root directory during import.

## Deploy to Vercel

1. Go to the Vercel dashboard and choose **New Project**.
2. Import the GitHub repository.
3. Use these settings:
   - Framework Preset: **Vite**
   - Root Directory: this folder, if it is inside a larger repo
   - Build Command: `npm run build`
   - Output Directory: `dist`
4. Click **Deploy**.

After that, every push to `main` creates a production deployment, and other branches get preview deployments.

## Custom Domain Later

1. Open the Vercel project.
2. Go to **Settings** > **Domains**.
3. Add your domain, such as `example.com` or `www.example.com`.
4. Follow Vercel's DNS instructions. Vercel will show the exact records to add at your domain registrar.
5. After DNS updates propagate, Vercel will provision SSL automatically.

Common setup:

- Apex/root domain, such as `example.com`: add an A record pointing to Vercel's IP.
- Subdomain, such as `www.example.com`: add a CNAME record pointing to Vercel's target.

Use the exact values shown inside your Vercel dashboard when you are ready to connect the real domain.
