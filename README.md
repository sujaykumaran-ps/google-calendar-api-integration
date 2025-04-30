# Meetings Dashboard

A simple vanilla-JavaScript dashboard that connects to your Google Calendar and shows:

- **Today’s meeting count**  
- **Clickable list** of today’s events (title + time)  
- **OAuth2** implicit-flow authorization—no backend required  

<p align="center">
  <img src="screenshot.png" alt="Dashboard screenshot" width="400"/>
</p>

## Features

- **Client-only**: pure HTML/JS; no build step or server-side code  
- **OAuth2 implicit flow**: redirects to Google’s consent screen, fetches an access token, and calls Calendar REST API  
- **Responsive UI**: displays count and event list; click an event to open it in Calendar  

## Tech Stack

- HTML5 & vanilla JavaScript  
- [Google OAuth2](https://developers.google.com/identity/protocols/oauth2) (implicit flow)  
- Google Calendar REST API  
- Static server (e.g. [http-server](https://www.npmjs.com/package/http-server) or Python’s `http.server`)

## Prerequisites

1. A Google Cloud project with:
   - **OAuth 2.0 Client ID** (type = Web application)  
     - Authorized JavaScript origin: `http://localhost:8000`  
     - Authorized redirect URI: same as above  
   - **Test user** added on the OAuth consent screen (for unverified apps)  
2. Your **Client ID** from GCP

## Getting Started

1. **Clone** this repo:
   ```bash
   git clone https://github.com/your-username/meetings-dashboard.git
   cd meetings-dashboard
