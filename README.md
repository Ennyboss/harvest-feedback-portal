# harvest-feedback-portal

A simple outreach webpage for collecting stakeholder feedback on the HARVEST tool (ICICLE AI Institute Fellowship Project)

## Project Structure

This is a static website project with the following structure:
- `index.html` - Main entry point (single-page application)
- `icicle-logo.jpg` - ICICLE logo image
- `Harvest_In_5_Steps_Guide.pdf` - PDF guide for users
- `.nojekyll` - Ensures GitHub Pages serves all files correctly

## Deployment to GitHub Pages

This project is configured to be deployed directly to GitHub Pages from the repository root.

### Deployment Configuration

- **Branch**: `main`
- **Publish directory**: Repository root (`/`)
- **Site URL**: `https://ennyboss.github.io/harvest-feedback-portal/`

### Local Development

To test the site locally, you can use Python's built-in HTTP server:

```bash
# Navigate to the project directory
cd harvest-feedback-portal-main

# Start a local server (Python 3)
python -m http.server 8000

# Open in browser
# http://localhost:8000
```

### GitHub Pages Considerations

- The `index.html` file must be at the publish root (repository root in this case)
- The `.nojekyll` file ensures GitHub Pages doesn't process files with Jekyll (important for PDF files and other assets)
- After enabling GitHub Pages, it may take a few minutes for the site to become available
- The site will automatically rebuild when you push changes to the `main` branch
