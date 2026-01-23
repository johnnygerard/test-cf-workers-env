# Cloudflare Workers Environment Test

The primary objective of this project is to demonstrate that environment variables loaded from a `.env` file can be overridden without modifying the source code. This functionality is driven by the environment loading priorities inherent to Vite, which serves as the underlying build tool for Astro. For further technical details, refer to the documentation on [Vite Environment Variables and Modes](https://vite.dev/guide/env-and-mode#env-files).

![project status](https://img.shields.io/badge/project_status-active-success?style=for-the-badge)
[![live site](https://img.shields.io/badge/live_site-blue?style=for-the-badge)](https://test-cf-workers-env.mail-25a.workers.dev/)

## Procedure to Override Build-Time Environment Variables

1. In the Cloudflare Workers dashboard ("Workers & Pages"), select the "Settings" tab of your worker.
2. Select the "Build" section on the page.
3. Look for "Variables and secrets" and click on "+ Add".
4. In the modal that appears, add your variable ("Variable name" and "Value" fields), then click "Save".
5. Go to "Deployments" tab and click on "View build history".
6. Find the latest build, click on the three dots on the right side, and select "Retry build".

## Tech Stack

### Frontend

- **Framework**: [Astro 5](https://astro.build/)
- **Styling**: [Tailwind CSS 4](https://tailwindcss.com/)

### Backend

- **Hosting**: [Cloudflare Workers](https://workers.cloudflare.com/)

## How to Update

To check for outdated packages, run `npm outdated`.

```bash
# Update dependencies (this will rewrite package-lock.json and package.json)
npm update --save
npm install --save-exact --save-dev prettier@latest prettier-plugin-astro@latest prettier-plugin-tailwindcss@latest
```

## Notes

- `.nvmrc` is used primarily as a way to specify the Node.js version for Cloudflare Workers (see [Build image](https://developers.cloudflare.com/workers/ci-cd/builds/build-image/))
- The GitHub Action `actions/setup-node@v6` relies on both `package.json` `engines` and `devEngines` to set the Node.js version and automatically cache npm dependencies.

## Dev Environment & Tools

- **System**: [Ubuntu](https://ubuntu.com/desktop)
- **Editor**: [VS Code](https://code.visualstudio.com/)
- **Formatter**: [Prettier](https://prettier.io/)
- **Linter**: [ESLint](https://eslint.org/)
- **AI assistant**: [GitHub Copilot](https://github.com/features/copilot)

## Copyright

© 2026 Johnny Gérard
