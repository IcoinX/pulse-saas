# PULSE SaaS Deployment Guide

## Quick Deploy Options

### Option 1: Render (Free Tier)
1. Push code to GitHub
2. Go to https://render.com
3. Create new Web Service
4. Connect GitHub repo
5. Build command: `npm install`
6. Start command: `node server.js`
7. Add env vars:
   - `SUPABASE_URL`: https://plojsqsjykzqwdaolfpi.supabase.co
   - `SUPABASE_SERVICE_KEY`: your_service_key
   - `JWT_SECRET`: random_secure_string
   - `STRIPE_SECRET_KEY`: sk_test_...

### Option 2: Railway
1. Go to https://railway.app
2. Create new project from GitHub
3. Add environment variables

### Option 3: Fly.io
1. `fly launch`
2. `fly deploy`

## Environment Variables
```
SUPABASE_URL=https://plojsqsjykzqwdaolfpi.supabase.co
SUPABASE_SERVICE_KEY=<your_key>
JWT_SECRET=<secure_random_string>
STRIPE_SECRET_KEY=sk_test_<your_stripe_key>
```

## Database Setup
Run schema.sql in Supabase SQL Editor.

## Verify
- Health: /api/health
- Tiers: /api/tiers
- Signup: POST /api/auth/signup
