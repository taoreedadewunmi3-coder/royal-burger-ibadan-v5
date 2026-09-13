# Royal Burger Ibadan — Vercel Full-Stack Website

React + Vite restaurant website with Vercel serverless API support.

## Pages
Home, Menu, About, Contact, Cart, Login/Signup and Admin.

## Vercel deployment
**Important:** Vercel must use the folder that contains `package.json`, `index.html`, `src/`, `api/`, and `vercel.json` as the project root.

If your GitHub repository contains a parent folder such as `royal-burger-upgrade/`, either:
- set Vercel **Root Directory** to `royal-burger-upgrade`, or
- move the contents of that folder to the repository root.

Build command: `npm run build`
Output directory: `dist`
Install command: `npm install`

## Environment variables
For Firebase, add these to Vercel Project Settings → Environment Variables:
- `VITE_FIREBASE_API_KEY`
- `VITE_FIREBASE_AUTH_DOMAIN`
- `VITE_FIREBASE_PROJECT_ID`
- `VITE_FIREBASE_STORAGE_BUCKET`
- `VITE_FIREBASE_MESSAGING_SENDER_ID`
- `VITE_FIREBASE_APP_ID`

For order receipts, add server-only variables:
- `RESEND_API_KEY`
- `RECEIPT_FROM_EMAIL`
- `WHATSAPP_ACCESS_TOKEN`
- `WHATSAPP_PHONE_NUMBER_ID`

Do not put private API keys in frontend source code.

## Local test
```bash
npm install
npm run dev
```

Production build:
```bash
npm run build
```

## Important
The site is designed to render even before Firebase environment variables are added. Firebase-dependent login/order features will require the variables above.
