# RobuxBulgaria-style safe demo

A dark, gold-accented Bulgarian demo storefront inspired by the form layout of the referenced page. This is not affiliated with Roblox or RobuxBulgaria, and it does not process real Robux orders.

## Safe data flow
- Nickname, phone number, and the 4-character demo code are only used locally in the browser.
- None of those fields are included in network requests, stored, or sent to Discord.
- The server receives only the selected demo package and generates a demo order ID.
- Discord receives only demo order ID, selected package, timestamp, and a clearly marked demo-only status.
- No SMS messages or account verification are performed.

## Run locally
1. Install Node.js 18 or newer.
2. In this folder, run `npm install`.
3. Copy `.env.example` to `.env`.
4. Optionally set `DISCORD_WEBHOOK_URL` in `.env` to a webhook you control.
5. Run `npm start`.
6. Visit `http://localhost:3000`.

Create the webhook through Discord Server Settings → Integrations → Webhooks. Keep its URL private. Do not place it in frontend files.

## Files
- `public/index.html`: Bulgarian form, package options, demo code step, help modal.
- `public/styles.css`: dark layout with gold accents.
- `public/app.js`: client-side interactions and safe submission.
- `server.js`: endpoint which receives package amount only and posts a demo embed.
- `package.json`: Node project settings.
- `.env.example`: server configuration template.
