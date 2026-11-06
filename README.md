Looproom
The third English-language tool site, with independent source code and no runtime dependencies or paid APIs. It works by double-clicking index.html. This site includes: Audio Speed Changer, AB Loop Player & Metronome.

Local Development and Build
No npm install is required. After installing Node.js:

text
npm run dev
npm test
npm run build
Local address: http://127.0.0.1:4175. Build output goes to dist. Online preview: https://looproom.luqihang594241.workers.dev/#tool

Deployment
It is recommended to use a separate GitHub repository and upload the contents of this directory. Cloudflare Pages: framework None, build command npm run build, output directory dist. When deploying from the same repository, set the root directory to looproom. The Workers static assets directory is also dist; use the static asset deployment configuration provided in the console.

In production, set SITE_URL=https://actual-domain (without a path). The build generates the canonical, og:url, sitemap, and robots sitemap address for that domain.
