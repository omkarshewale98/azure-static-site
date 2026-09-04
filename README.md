# Azure Static Website

A simple static HTML website hosted on an Azure Ubuntu VM using nginx.

## Architecture

Developer
   |
   | Pull Request
   v
GitHub
   |
   | CI
   v
HTML Linter
   |
   | Merge to main
   v
GitHub Actions
   |
   | SSH/SCP
   v
Azure VM
   |
   v
nginx
   |
   v
/var/www/app
   |
   v
index.html

## Technologies

- Azure VM
- Ubuntu 22.04
- nginx
- GitHub Actions
- HTML

## Deployment

A pull request runs HTML validation.

After merging to `main`, GitHub Actions copies `index.html` to the Azure VM and reloads nginx.

## Public URL

http://YOUR_VM_IP
