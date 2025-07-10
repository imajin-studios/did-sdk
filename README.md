# Issuer SDK Distribution

This directory contains the browser-ready bundle of the Issuer SDK.

## How to Deploy (GitHub Pages)

1. **Commit and push the `dist/` directory to your repository.**
2. **Go to your repo settings > Pages.**
3. **Set the source to `/frontend/dist` (or `/dist` if at root).**
4. **Your SDK will be available at:**
   `https://<your-username>.github.io/<repo-name>/issuer-sdk.min.js`

## How to Use (for Shops)
```html
<script src="https://<your-username>.github.io/<repo-name>/issuer-sdk.min.js"></script>
<script>
  const client = new window.sdk.IssuerSDK('YOUR_API_KEY');
  // ...
</script>
```

## For Production
- Always build a fresh bundle before release: `npx rollup -c frontend/rollup.config.js`
- Host on a CDN or static host for best performance and reliability.
- Update the API base URL in `sdk.js` to your production backend before bundling. 