# PULSE Protocol SaaS

Event streaming infrastructure for AI agents.

## Quick Start

### 1. Set up Supabase Database

Run the SQL in `supabase/schema.sql` in your Supabase SQL Editor.

### 2. Configure Environment

Create `.env` file:

```bash
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_SERVICE_KEY=your-service-key
JWT_SECRET=your-jwt-secret
STRIPE_SECRET_KEY=sk_test_xxx  # Optional
```

### 3. Start API Server

```bash
npm install
npm start
```

Server runs on port 3001.

### 4. Deploy Landing Page

Deploy `index.html` to GitHub Pages or any static host.

## API Endpoints

### Events
- `POST /api/events` - Emit event (requires X-API-Key)
- `GET /api/events` - List events (requires X-API-Key)

### API Keys
- `GET /api/keys` - List your API keys (requires Bearer token)
- `POST /api/keys` - Generate new API key (requires Bearer token)
- `POST /api/keys/:id/revoke` - Revoke API key (requires Bearer token)

### Subscriptions
- `GET /api/subscription` - Get current subscription
- `POST /api/subscription/create-checkout` - Create Stripe checkout

## Pricing

- **Free**: $0/mo - 1K events/month
- **Pro**: $49/mo - 50K events/month
- **Enterprise**: $499/mo - 500K events/month

## Deployment

### GitHub Pages

```bash
git checkout -b pulse-saas
git add .
git commit -m "PULSE SaaS v1.0"
git push -u origin pulse-saas
```

Enable GitHub Pages on the `pulse-saas` branch at:
`https://github.com/IcoinX/openclaw-workspace/settings/pages`
