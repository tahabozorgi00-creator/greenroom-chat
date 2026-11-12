# GreenRoom — friends chat

A dark, military-green themed chat website starter. It includes email/password accounts, invite-code chat rooms, message history, and real-time messages using Supabase.

## What is included
- Sign up and sign in with Supabase Auth
- Create a private room and get a 6-character invite code
- Join a friend's room with their code
- Send and receive live text messages
- Row Level Security policies for room membership and messages

## Setup

### 1. Create the backend
1. Create a project at https://supabase.com.
2. Open **Project Settings → API** and copy the Project URL and anon/public key.
3. In **SQL Editor**, run all of `supabase/schema.sql`.
4. In **Authentication → URL Configuration**, set your local site URL to `http://localhost:5173` while testing. For a deployed site, add its real URL too.
5. For quick testing, you can turn off email confirmation in **Authentication → Providers → Email**. For a public site, keep email confirmation enabled.

### 2. Configure the website
1. Install Node.js (LTS).
2. Copy `.env.example` to a new file named `.env`.
3. Fill in `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY`.
4. In this folder, run:

```bash
npm install
npm run dev
```

5. Open the local URL Vite prints, usually `http://localhost:5173`.

### 3. Put it online
Deploy the project to a static hosting provider such as Vercel or Netlify. Set the same two `VITE_SUPABASE_*` environment variables in the hosting dashboard, then add your deployed domain to Supabase Auth's allowed redirect/site URLs.

## Important notes
- This is a working starter, not a hosted website. It needs your own Supabase project and deployment account before friends can use it online.
- Do not put a Supabase **service_role** key in `.env` or frontend code. Only use the anon/public key.
- Invite codes are convenient for a small private group, but anyone who gets a code can join that room. Share codes only with people you trust.
- This first version supports text chat and rooms. Voice/video calls, direct messages, image uploads, message moderation, and stronger invite management are not included yet.
- Add appropriate moderation, blocking/reporting, rate limits, and privacy rules before opening it to a wider audience.
