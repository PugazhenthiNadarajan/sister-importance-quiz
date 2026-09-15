# Sister Verification & Importance Quiz (Vercel Deployment Guide)

This web application is configured and ready for 1-click deployment on **[Vercel](https://vercel.com)**.

---

## Project Structure
```
sister-quiz/
├── index.html          # Interactive Tanglish Quiz Frontend (Tailwind + Confetti + Web Audio)
├── vercel.json         # Vercel deployment & routing config
├── package.json        # Project metadata
├── api/
│   └── send-email.js   # Vercel Serverless Function (Direct Resend API backend)
└── README.md           # Deployment documentation
```

---

## How to Host on Vercel (Choose Method 1 or 2)

### Method 1: Deploy via GitHub & Vercel Dashboard (Easiest - 2 Minutes)
1. **Push to GitHub**:
   - Create a new repository on GitHub (e.g. `sister-importance-quiz`).
   - Push this folder to your repository:
     ```bash
     git init
     git add .
     git commit -m "Initial commit for Vercel"
     git branch -M main
     git remote add origin https://github.com/<YOUR_USERNAME>/sister-importance-quiz.git
     git push -u origin main
     ```
2. **Import on Vercel**:
   - Go to **[vercel.com/new](https://vercel.com/new)** and sign in with your GitHub account.
   - Select your `sister-importance-quiz` repository.
   - Click **Deploy**.
3. **Done!** Vercel gives you an instant live URL like `https://sister-importance-quiz.vercel.app`!
   - Send this link to your sister on WhatsApp!

---

### Method 2: Deploy using Vercel CLI
If you have Node.js installed, open terminal in this folder and run:
```bash
npx vercel
```
Follow the prompts (choose defaults by pressing Enter). Vercel will upload and provide your live URL in 30 seconds!

---

## Features on Vercel
1. **Serverless Email API (`/api/send-email`)**: When hosted on Vercel, the app automatically routes through the serverless function to dispatch the full report via Resend API directly to `pugazh2006nadarajan@gmail.com`.
2. **Automatic Fallback to FormSubmit**: If running locally or without serverless, it seamlessly uses the FormSubmit AJAX gateway.
3. **WhatsApp & Mail Instant Share**: Her final verdict can be shared with one click.
