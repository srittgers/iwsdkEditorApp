# IWSDK Starter Template

This folder is a source template used by `scripts/generate-starters.cjs` to produce 8 runnable variants:

- `starter-<vr|ar>-<manual|metaspatial>-<ts|js>`

Do not run this template directly. The generator will:

- Copy a variant-specific `src/index.ts` (see `src/index-*.ts`).
- Install the matching Vite config from `configs/`.
- Keep only the required metaspatial folder (renamed to `metaspatial`).
- Prune unused assets and dev dependencies.

UI is defined in `ui/welcome.uikitml`; the Vite UIKitML plugin compiles it to `public/ui/welcome.json` during build in generated variants.

## GitHub Pages Deployment

This application is automatically deployed to GitHub Pages when changes are pushed to the `main` branch.

### Setup Instructions

1. **Enable GitHub Pages in your repository:**
   - Go to your repository Settings
   - Navigate to "Pages" section
   - Under "Build and deployment", select "GitHub Actions" as the source

2. **Push to main branch:**
   - Any push to the `main` branch will trigger the deployment workflow
   - The site will be available at: `https://srittgers.github.io/iwsdkEditorApp/`

3. **Manual deployment:**
   - You can also trigger deployment manually from the "Actions" tab
   - Select the "Deploy to GitHub Pages" workflow
   - Click "Run workflow"

### Local Development

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

