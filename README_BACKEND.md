# VedParts Node.js backend starter

This is the first deployment checkpoint for VedParts. It uses the same style as the VedChat backend: JavaScript, CommonJS (`require`), and Node.js's built-in `http` module.

## What works in this starter
- `GET /` returns a JSON service status.
- `GET /health` returns `{"ok":true,"service":"vedparts-api"}`.
- Uses Render's `PORT` environment variable.

## Important limitation
This is only a health-check starter. It does **not** yet store inventory, authenticate users, or record sales. Do not enter real stock data into it. The next step is to configure a persistent database and authenticated inventory endpoints; Render's local filesystem must not be used for permanent stock records.

## Deploy on Render
1. Put `server.js`, `package.json`, and `.gitignore` in the root of your GitHub `VedParts` repository. Keep your existing README.
2. In Render, create a **Web Service** and connect the `VedParts` GitHub repository.
3. Set **Runtime** to Node.
4. Set **Build Command** to `npm install`.
5. Set **Start Command** to `npm start`.
6. Choose the **Free** instance type, if available for your account/region, then deploy.
7. When deployment finishes, open the service URL followed by `/health`. A successful response is JSON containing `"ok": true`.

## Security and cost
- Never commit passwords, API keys, database credentials, or `.env` files to GitHub.
- This starter has no database and no authentication. Do not treat the public health endpoint as a protected inventory API.
- Render's free service may sleep when idle. Free-tier limits and availability can change.
