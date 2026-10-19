# AquaSense GitHub Pages

This folder contains the static dashboard for GitHub Pages. Node-RED and MySQL continue running on your server; Pages only serves the frontend.

## Before publishing

1. Set a public HTTPS/WSS endpoint for the Node-RED WebSocket path `/ws/water`.
2. Copy `config.js.example` to `config.js` and replace the sample host with that endpoint, for example `wss://nodered.example.com/ws/water`.
3. Publish the contents of this folder as the repository root (or use it as the Pages publishing folder).
4. In GitHub, open **Settings → Pages** and select the branch/folder to publish.

The dashboard expects JSON telemetry and control messages over the WebSocket. Do not put passwords, access tokens, broker credentials, or other secrets in `config.js` or the HTML. Configure access controls on the Node-RED server before exposing control actions to the internet.