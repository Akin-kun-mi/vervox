# VerVox Landing Page
This is a static, highly-optimized HTML landing page for VerVox.

## How to Deploy to GitHub Pages (Automated & Secure)
We have included a GitHub Actions workflow that will automatically deploy your site whenever you push changes to the `main` branch. This is secure, free, and sets up HTTPS automatically.

### Step 1: Push to GitHub
If you haven't already, push this code to a new private GitHub repository:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

### Step 2: Enable GitHub Actions
1. Go to your repository on GitHub.
2. Click **Settings** > **Pages** (on the left sidebar).
3. Under **Build and deployment**, change the **Source** dropdown to **GitHub Actions**.

### Step 3: Trigger the Build
1. GitHub will automatically detect the `.github/workflows/deploy.yml` file.
2. Any time you push to the `main` branch, the site will automatically build and deploy.
3. You can see the progress in the **Actions** tab on your repository.

### Step 4: Add Your Custom Domain (Optional)
If you bought a domain (like `vervox.com`):
1. In the repository **Settings** > **Pages**, add your custom domain.
2. Update your DNS provider (GoDaddy, Namecheap, etc.) to point the CNAME record to `YOUR_USERNAME.github.io`.

### Security Note
- Your built-in `.gitignore` ensures that you will never accidentally commit secure OS files, environments secrets (`.env`), or heavy node packages if you decide to expand the site in the future.
- The workflow specifically requests only the permissions needed to upload the frontend build (`id-token: write`, `pages: write`), ensuring least-privilege security.
