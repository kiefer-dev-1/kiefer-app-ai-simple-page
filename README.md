# Kiefer Company Website

A simple company website for Kiefer, a renewable energy solutions provider.

## Overview

This repository contains a GitHub Pages website for Kiefer, showcasing the company's services, projects, and contact information. The site is designed to be hosted on the domain kiefer-app.ai.

## Setup Instructions

### 1. GitHub Repository Setup

1. Create a new GitHub repository (or use an existing one)
2. Push this code to the repository
3. GitHub Actions will automatically deploy the site to GitHub Pages when you push to the main branch
4. Alternatively, you can enable GitHub Pages in the repository settings:
   - Go to Settings > Pages
   - Select the branch to deploy (usually `main` or `master`)
   - Click Save

### 2. Automated Deployment with GitHub Actions

This repository includes GitHub Actions workflows for testing and deploying the website:

#### Combined Workflow

A combined workflow is included to run all checks at once:

- The workflow is defined in `.github/workflows/all-checks.yml`
- It can be manually triggered from the Actions tab
- It runs all the checks described below in parallel
- This is useful for comprehensive testing during development

#### Deployment Workflow

The main workflow automatically deploys the website to GitHub Pages whenever changes are pushed to the main branch:

- The workflow is defined in `.github/workflows/deploy.yml`
- It uses GitHub's official actions for deploying to GitHub Pages
- No manual steps are required after pushing changes to the repository
- You can also manually trigger the workflow from the Actions tab in your repository

#### Testing Workflow

A test workflow is included to verify the repository setup before deployment:

- The workflow is defined in `.github/workflows/test.yml`
- It can be manually triggered from the Actions tab in your repository
- It verifies that all necessary files exist and are correctly configured
- Use this workflow to troubleshoot any issues with the GitHub Pages setup

#### Validation Workflow

A validation workflow is included to check HTML and CSS code quality:

- The workflow is defined in `.github/workflows/validate.yml`
- It runs automatically on pull requests to the main branch
- It can also be manually triggered from the Actions tab
- It validates HTML files using html-validate
- It validates CSS files using stylelint
- This helps maintain code quality and consistency

#### Link Checking Workflow

A link checking workflow is included to detect broken links:

- The workflow is defined in `.github/workflows/link-check.yml`
- It runs automatically on a weekly schedule (Sunday at midnight)
- It can also be manually triggered from the Actions tab
- It checks for broken links in both local HTML files and the deployed site
- This helps ensure all links on the website are working properly

#### Accessibility Checking Workflow

An accessibility checking workflow is included to ensure the website is accessible to all users:

- The workflow is defined in `.github/workflows/accessibility.yml`
- It runs automatically on pull requests to the main branch
- It can also be manually triggered from the Actions tab
- It uses pa11y to check for accessibility issues in the website
- This helps ensure the website is accessible to users with disabilities

#### Performance Checking Workflow

A performance checking workflow is included to ensure the website loads quickly:

- The workflow is defined in `.github/workflows/performance.yml`
- It runs automatically on pull requests to the main branch
- It can also be manually triggered from the Actions tab
- It uses Lighthouse CI to check for performance issues in the website
- Performance thresholds are defined in `lighthouserc.json`:
  - Performance score: minimum 90%
  - Accessibility score: minimum 90%
  - Best practices score: minimum 90%
  - SEO score: minimum 90%
  - First contentful paint: maximum 2000ms
  - Time to interactive: maximum 3500ms
  - Largest contentful paint: maximum 2500ms
- This helps ensure the website provides a good user experience

#### Security Scanning Workflow

A security scanning workflow is included to detect security vulnerabilities:

- The workflow is defined in `.github/workflows/security.yml`
- It runs automatically on a weekly schedule (Monday at midnight)
- It can also be manually triggered from the Actions tab
- It uses OWASP ZAP to scan for security vulnerabilities in the website
- A security report is generated and uploaded as an artifact
- This helps ensure the website is secure and protected against common security threats

### 3. Custom Domain Setup

1. Configure your domain (kiefer-app.ai) with your domain registrar:
   - Add an A record pointing to GitHub Pages IP addresses:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - Or add a CNAME record pointing to your GitHub Pages URL (`yourusername.github.io`)

2. The CNAME file in this repository is already set up with the domain `kiefer-app.ai`

3. In your GitHub repository settings:
   - Go to Settings > Pages
   - Under "Custom domain", enter `kiefer-app.ai`
   - Check "Enforce HTTPS" (recommended)
   - Click Save

### 4. Wait for DNS Propagation

It may take up to 24 hours for DNS changes to propagate. Once propagation is complete, your site will be accessible at kiefer-app.ai.

## Local Development

To view the site locally, simply open the `index.html` file in a web browser.   

## Technologies Used

- HTML5
- CSS3
- Font Awesome for icons
- Google Fonts (Roboto)

## Contributing

### Reporting Issues

If you encounter any issues with the website, please report them using the GitHub issue templates:

1. Go to the Issues tab in the repository
2. Click on "New Issue"
3. Choose the appropriate template:
   - **Bug Report**: For reporting website errors or problems
   - **Feature Request**: For suggesting new features or improvements

Please provide as much detail as possible when reporting issues to help us address them quickly.

### Development Workflow

1. Fork the repository
2. Create a new branch for your feature or bugfix
3. Make your changes
4. Test your changes locally
5. Submit a pull request using the provided pull request template
   - Fill out all relevant sections of the template
   - Link to any related issues
   - Provide screenshots if applicable
6. Wait for review and address any feedback
7. The GitHub Actions workflow will automatically deploy your changes once merged
