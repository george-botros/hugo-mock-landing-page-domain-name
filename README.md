# BetterSpend Hugo Deployment

## Overview
This repository is an auto-deployed version of the `hugo-mock-landing-page` project. It leverages **GitHub Actions** to automate the process of building and deploying the Hugo-based static website to **GitHub Pages**.

# BetterSpend Hugo Deployment

## Overview
This repository, `hugo-mock-landing-page-autodeployed`, is an auto-deployed version of the `hugo-mock-landing-page` project. It leverages **GitHub Actions** to automate the process of building and deploying the Hugo-based static website to **GitHub Pages**.

## About BetterSpend
BetterSpend is a smart budgeting application designed to help users track their spending habits, forecast cash flow, and optimize savings effortlessly. With AI-driven insights, real-time budget alerts, and personalized financial recommendations, BetterSpend empowers users to take control of their finances and make informed decisions.

### Key Features:
- **Smart Spending Insights**: Get a breakdowns of your spending trends.
- **Real-Time Alerts**: Receive notifications when you're approaching budget limits or detecting unusual transactions.
- **Cash Flow Forecasting**: Plan ahead with intelligent predictions of future expenses.
- **Custom Budget Categories**: Set personalized budgets for different spending areas.
- **Automated Savings Recommendations**: Discover opportunities to save money based on your habits.
- **Goal Tracking**: Set and achieve financial goals with detailed progress tracking.

## GitHub Actions Workflow
The repository includes a **GitHub Actions workflow** located in `.github/workflows/gh-pages-deployment.yaml`, which automates the following steps:

1. **Trigger on Push**: The workflow runs automatically whenever changes are pushed to the `main` branch.
2. **Checkout Source Code**: It fetches the latest code from the repository, including submodules for themes.
3. **Set Up Hugo**: Initializes the Hugo environment using the latest extended version.
4. **Build the Static Site**: Generates the Hugo static website with optimizations (`--gc --minify`).
5. **Deploy to GitHub Pages**: Publishes the output to the `gh-pages` branch using `peaceiris/actions-gh-pages`.

## Deployment URL
Once the workflow runs successfully, the website is deployed and accessible at:

[https://george-botros.github.io/hugo-mock-landing-page-autodeployed/](https://george-botros.github.io/hugo-mock-landing-page-autodeployed/)

## Configuration Changes
To ensure correct deployment, the following changes were made:
- **Updated `config.toml`**: The `baseURL` was modified to match the new repository name.
- **Enabled GitHub Actions Permissions**: Set **Read and Write** permissions for the workflow.
- **Activated GitHub Pages**: Configured the `gh-pages` branch as the publishing source.

## Running Locally
To preview changes locally before pushing:
```bash
hugo server -D
```
Then visit `http://localhost:1313/` in your browser.

## Making Updates
To update the website:
1. Make changes in the `main` branch.
2. Commit and push the changes.
3. The GitHub Actions workflow will automatically rebuild and deploy the site.

## Troubleshooting
- If the workflow fails, ensure **GitHub Actions permissions** are correctly configured.
- If the website does not update, force refresh your browser cache (`Ctrl+Shift+R`).
- Check the **Actions tab** in GitHub for logs and debugging.