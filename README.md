# Selva Prime Studio

A mobile-first prototype for **Selva Prime**, a fashion label in Accra, Ghana. One voice note and a photo become a week of social posts in the founder's voice, ready to approve in under 25 minutes a week.

Built by the Pink Panthers for the SheConsult SME Innovation Challenge.

## What's inside

A single static page, `index.html`, with no build step:

- **Studio:** pick a piece (or let the AI pick), add a note, make the week.
- **Week:** four posts with previews for Instagram, TikTok, Pinterest, WhatsApp Status and Google; approve, schedule or post now.
- **Plan:** posting times for Accra, London and New York.
- **Results:** reach, chats and the weekly time meter.
- **Ideas:** lessons from past posts plus a two-week content calendar.
- **Leads:** a WhatsApp/Instagram assistant that collects custom-order details; the founder sets every quote.

## Sample mode vs live AI

On claude.ai the page uses the viewer's Claude account for live writing and voice notes. Hosted anywhere else (for example Vercel), those calls aren't available, so the app uses its **labelled sample content** instead. Every screen still works.

Posting is simulated. Results and enquiries are sample data and are labelled as such.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy to Vercel

Import this repository at vercel.com (framework preset: **Other**, no build command, output directory: root), or from this folder:

```bash
npx vercel --prod
```

Note: Vercel's free Hobby plan is for non-commercial use. For the business's own production use, use a Pro plan or a host whose free tier allows commercial use.

## Next step

Live AI on Vercel needs a small server function (`/api/generate`) that calls Claude with an API key kept as a Vercel environment variable, plus rate limiting.
