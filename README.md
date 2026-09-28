# Atlassian Exit Planner

A static, single-page tool for teams leaving Atlassian Server / Data Center.

1. Pick the Atlassian products you run (Jira Software, Jira Service Management, Confluence, Bitbucket, Bamboo, Crowd, Marketplace apps).
2. Pick the platforms to compare: Azure DevOps Server, GitHub Enterprise Server, an open-source stack, and Data Center as a baseline.
3. Mark how much each feature matters (Not used / Nice / Should / Must).
4. Run the analysis to get a fit score per platform and per product, must-have gaps, a feature mapping table and a recommendation.

No backend, no build step, no dependencies. Answers are kept in the browser's local storage only.

## Publish on GitHub Pages

1. Create a repository and push this folder (`index.html`, `.nojekyll`, `README.md`).
2. Go to **Settings → Pages**, set **Source** to *Deploy from a branch*, and choose `main` / `/ (root)`.
3. The site appears at `https://<org>.github.io/<repo>/`.

On GitHub Enterprise Server, Pages must be enabled by your site admin first.

## Updating the feature ratings

All products, features, descriptions and ratings live in the `TOOLS` array in `index.html`.
Each feature is `[id, category, name, description, azureDevOps, githubES, openSource, note]`,
with ratings `N` (native), `P` (partial), `A` (add-on / extra licence) or `X` (not available).

Ratings are a general assessment as of Sep 2026, not vendor-certified.
