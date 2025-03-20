# Kiefer Company Website

A simple company website for Kiefer, a renewable energy solutions provider.

## Overview

This repository contains a GitHub Pages website for Kiefer, showcasing the company's services, projects, and contact information. The site is designed to be hosted on the domain kiefer-app.ai.

## Setup Instructions

### 1. GitHub Repository Setup

1. Create a new GitHub repository (or use an existing one)
2. Push this code to the repository
3. Enable GitHub Pages in the repository settings:
   - Go to Settings > Pages
   - Select the branch to deploy (usually `main` or `master`)
   - Click Save

### 2. Custom Domain Setup

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

### 3. Wait for DNS Propagation

It may take up to 24 hours for DNS changes to propagate. Once propagation is complete, your site will be accessible at kiefer-app.ai.

## Local Development

To view the site locally, simply open the `index.html` file in a web browser.

## Technologies Used

- HTML5
- CSS3
- Font Awesome for icons
- Google Fonts (Roboto)
