# Academic Website Template

A modern, responsive academic personal website template built with React, TypeScript, and Tailwind CSS.

## Features

- 🌍 Multi-language support (English and Japanese)
- 📱 Responsive design for all devices
- 📊 Dynamic publications section with filtering by year
- 📝 Markdown content support
- 🎨 Customizable theming
- 🚀 Easy deployment to GitHub Pages

## Getting Started

For a detailed guide on how to customize and use this template, please refer to the [wiki/procedure_for_user.md](wiki/procedure_for_user.md).

日本語での説明は[procedure_for_user_jp.md](wiki/procedure_for_user_jp.md)

### Prerequisites

- Node.js (v16 or later recommended)
- npm or yarn

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/academic-website.git
   cd academic-website
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn
   ```

3. Start the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. Open `http://localhost:3000` in your browser.

## Project Structure

- `/data` - CSV data files for publications
- `/public` - Static assets and content
  - `/api` - Generated JSON API files
  - `/content` - Markdown and JSON content files
  - `/images` - Images
  - `/locales` - Translation files
- `/scripts` - Utility scripts
- `/src` - Source code
  - `/components` - React components
  - `/hooks` - Custom React hooks
  - `/types` - TypeScript type definitions
  - `/utils` - Utility functions

## Customization

### Content

1. Update personal information in `/public/locales/en/translations.json` and `/public/locales/ja/translations.json`
2. Replace bio content in `/public/content/bio/`
3. Add your profile picture to `/public/images/profile.jpg`
4. Update your publication data in `/data/rm_published_papers.csv` and `/data/rm_presentations.csv`
5. Add awards, grants, and projects data in `/public/content/awards/`
6. Update career data in `/public/content/career/`

### Styling

1. Customize colors and theme in `tailwind.config.js`
2. Modify global styles in `src/index.css`

## Deployment

This template is configured for easy deployment to GitHub Pages using GitHub Actions. Follow these steps to deploy your site:

1. Go to the "Actions" tab in your forked repository.
2. Find and select the "Deploy to GitHub Pages" workflow.
   - If the workflow is already running or completed, check the results.
   - If the workflow is not found, create it by navigating to the `.github/workflows` directory and ensuring a `deploy.yml` file exists. If not, create a new one and copy the content from the template repository.
3. Once the workflow succeeds, go to "Settings" → "Pages" to verify the published URL.

> **Tip**: The initial deployment may take a few minutes. Please be patient.

To rerun the deployment workflow if needed:

1. Click on the "Actions" tab in your repository.
2. Select "Deploy to GitHub Pages" from the "Workflows" list on the left.
3. Click the "Run workflow" button on the right.
4. Click "Run workflow" again to start the process.

## License

This template is MIT licensed. Feel free to modify and use it for your own academic website.

## Acknowledgements

- [Tailwind CSS](https://tailwindcss.com/)
- [React](https://reactjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Vite](https://vitejs.dev/)
- [i18next](https://www.i18next.com/)
