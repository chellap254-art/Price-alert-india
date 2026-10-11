# Price Alert India — starter project

A responsive static website for a future multi-store price-alert service.

## Current working features
- Product watchlist and store selection
- Current and target price fields
- Browser-local storage
- Target-price status and optional browser notifications
- Manual price updates
- Responsive mobile UI

## What is not automatic yet
This is not yet a live retailer price aggregator. Prices are user-entered. Amazon, Flipkart, Myntra, Croma, Reliance Digital, and other retailers require a permitted price source (official API, affiliate product feed, or a licensed provider), plus a backend to check prices on a schedule and send reliable notifications. Retailer access and terms vary.

Do not put API keys in `index.html` or any public GitHub repository. GitHub Pages only hosts static files; it does not run a private server or scheduled jobs.

## Publish using GitHub Pages
1. Download this ZIP and extract it on your phone/computer.
2. In your `price-alert-india` repository, choose **Add file → Upload files**.
3. Upload `index.html` and `README.md` from the extracted folder (not the ZIP itself).
4. Commit changes.
5. Open **Settings → Pages**.
6. Select **Deploy from a branch**, choose your default branch (usually `main`) and folder `/ (root)`, then save.
7. Wait for the website URL to appear in Settings → Pages.

## To build the automatic version
1. Choose an authorized price-data provider that covers the retailers you need.
2. Create a backend/serverless function and store provider credentials as server-side secrets.
3. Schedule checks (for example every few hours, subject to provider limits).
4. Store product records, price history, user alert thresholds, and notification preferences in a database.
5. Send notifications through an approved email or push-notification provider.
6. Add provider-specific adapters so future stores can be connected without rebuilding the whole site.

## Privacy
This demo saves the watchlist in local storage in the current browser. It does not upload the watchlist to a server. Clearing browser storage can erase it.
