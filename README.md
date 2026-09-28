# DevOps Platform Planner

A static, single-page tool for choosing where to move your DevOps and ALM tools on-prem.

1. Pick the tools you run today: Atlassian (Jira, JSM, Confluence, Bitbucket, Bamboo, Crowd, Marketplace apps), CI/CD & code (Jenkins, GitLab, TeamCity, SVN/Perforce, TFS), ALM & test (OpenText ALM, IBM ELM, TestRail, Jira Align), artifacts & quality (Artifactory/Nexus, SonarQube), ITSM (ServiceNow/BMC) and wikis (SharePoint/MediaWiki).
2. Pick the platforms to compare: Azure DevOps Server, GitHub Enterprise Server, GitLab Self-Managed, an open-source stack, and your current tools as a baseline.
3. Mark how much each feature matters (Not used / Nice / Should / Must).
4. Run the analysis to get a fit score per platform and per product, must-have gaps, a feature mapping table and a recommendation.

No backend, no build step, no dependencies. Answers are kept in the browser's local storage only.

## Publish on GitHub Pages

1. Create a repository and push this folder (`index.html`, `.nojekyll`, `README.md`).
2. Go to **Settings → Pages**, set **Source** to *Deploy from a branch*, and choose `main` / `/ (root)`.
3. The site appears at `https://<user>.github.io/<repo>/`.

On GitHub Enterprise Server, Pages must be enabled by your site admin first.

## Updating the feature ratings

All products, features, descriptions and ratings live in the `TOOLS` array in `index.html`.
Each feature is `[id, category, name, description, ratings, note]`, where `ratings` is a
4-letter string in the order Azure DevOps Server, GitHub ES, GitLab, open source (e.g. `"NPAX"`), using `N` (native), `P` (partial), `A` (add-on / extra licence) or `X` (not available).

Ratings are a general assessment as of Sep 2026, not vendor-certified.
