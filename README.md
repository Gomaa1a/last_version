# HireReady

AI-powered interview practice that helps students, graduates, and career switchers ace their next interview. Practice with a tough AI interviewer and get a detailed performance report.

## Tech Stack

- **Frontend:** React 18, TypeScript, Vite
- **UI:** shadcn/ui, Tailwind CSS, Radix UI
- **Backend:** Supabase (Auth, Database, Edge Functions)
- **AI:** OpenAI, ElevenLabs (TTS)
- **Deployment:** Vercel (frontend), Supabase (edge functions)

## Getting Started

### Prerequisites

- Node.js 18+ and npm

### Setup

```sh
# Clone the repo
git clone https://github.com/Gomaa1a/last_version.git
cd last_version

# Install dependencies
npm install

# Copy environment variables and fill in your values
cp .env.example .env

# Start the dev server
npm run dev
```

### Environment Variables

Copy `.env.example` to `.env` and fill in:

| Variable | Description |
|---|---|
| `VITE_SUPABASE_PROJECT_ID` | Your Supabase project ID |
| `VITE_SUPABASE_PUBLISHABLE_KEY` | Supabase anon/public key |
| `VITE_SUPABASE_URL` | Supabase project URL |

### Supabase Edge Functions

Edge functions require these secrets (set via Supabase dashboard or CLI):

- `LOVABLE_API_KEY` — AI gateway
- `ELEVENLABS_API_KEY` — Text-to-speech
- `OPENAI_API_KEY` — Realtime sessions
- `SUPABASE_URL`, `SUPABASE_ANON_KEY`, `SUPABASE_SERVICE_ROLE_KEY`

## Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start dev server on port 8080 |
| `npm run build` | Production build to `dist/` |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint |
| `npm test` | Run tests |

## Deployment

### Vercel (Frontend)

1. Connect the GitHub repo to Vercel
2. Framework preset: **Vite** (auto-detected)
3. Set environment variables in Vercel dashboard
4. Deploy

### Supabase (Edge Functions)

Deploy edge functions separately via Supabase CLI:

```sh
supabase functions deploy
```
