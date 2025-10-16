# Overview
This is a simple Bootstrap-based web page that looks up a GitHub user's account creation date using the public GitHub API. It includes:
- A form with id="github-user-" to enter the GitHub username.
- Optional support for adding a personal access token via the URL query string (?token=...), which can help avoid rate limits.
- The creation date is displayed in the element with id="github-created-at".

# Setup
No build steps are required.

- Option 1: Open index.html directly in your browser.
- Option 2: Serve it via any static server (recommended for consistent behavior with URL query parameters).

Example using npx:
- npx serve . 
- Then open http://localhost:3000

# Usage
- Enter a GitHub username and click "Lookup".
- The account creation date will appear under "Created At".

Optional:
- Append your GitHub token to the URL to increase rate limits:
  - Example: index.html?token=YOUR_GITHUB_TOKEN
- You can also prefill the username via URL:
  - index.html?username=octocat
  - index.html?user=octocat

On initial load, if no username is provided, the page will default to fetching details for "octocat".