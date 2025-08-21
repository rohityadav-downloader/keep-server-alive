# Keep Server Alive

This repository contains a GitHub Actions workflow that automatically makes GET requests to keep a server alive by preventing it from going to sleep due to inactivity.

## How it works

- The workflow runs every 5 minutes using GitHub Actions cron schedule
- It makes a GET request to the specified URL to keep the server active
- This prevents services like Render free tier from sleeping due to inactivity

## Target URL

The workflow pings: `https://tiktok-downloader-dej3.onrender.com/`

## Setup

1. Fork or clone this repository
2. The GitHub Actions workflow will automatically start running
3. You can monitor the workflow runs in the "Actions" tab of your repository

## Configuration

The workflow is configured in `.github/workflows/keep-alive.yml`. You can modify:

- The cron schedule (currently every 5 minutes)
- The target URL
- Add multiple URLs if needed

## Notes

- GitHub Actions has usage limits for free accounts
- The workflow will only run while the repository is active
- Consider the implications of frequent requests on your server
