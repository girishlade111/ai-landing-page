# AI Landing Page

A dark, premium landing page for an AI automation agency — originally generated with [v0.app](https://v0.app). Pitches AI workflow automation, intelligent chatbots, and 24/7 AI agents for businesses, with pricing, contact, and legal pages included.

## What it does

- Markets an AI services/agency business: workflow automation, chatbots, AI agents.
- Multi-section single-page layout: navbar, hero with 3D scene, features, pricing, contact, footer.
- Includes standalone `/privacy` and `/terms` pages.

## Features

- **Cinematic hero** — Spline 3D scene + animated gradient background, spotlight and sparkles effects.
- **Bento grid** feature showcase with Lucide icons.
- **Pricing section** with tiered plan cards.
- **Contact section** with business details and social links.
- **Privacy Policy & Terms** pages out of the box (`/privacy`, `/terms`).
- **Responsive navbar** component; dark-first Tailwind styling.
- Fully **static-exportable** (`output: "export"` in `next.config.mjs`) — deployable to any static host.

## Tech stack

- **Next.js 15** (App Router) + **React 19** + **TypeScript**
- **Tailwind CSS** + shadcn/ui-style components (button, card, label, switch, navbar, pricing)
- **@splinetool/react-spline** (3D hero scene), animated gradient / spotlight / sparkles effects
- **Lucide React** icons, **next-themes**
- Package manager: pnpm (`pnpm-lock.yaml`)

## Quick start

```bash
# 1. Clone
git clone https://github.com/girishlade111/ai-landing-page.git
cd ai-landing-page

# 2. Install dependencies
pnpm install        # or: npm install --legacy-peer-deps

# 3. Run the dev server
pnpm dev            # or: npm run dev
```

Open http://localhost:3000 in your browser.

### Build (static export)

```bash
pnpm build          # or: npm run build
```

The static site is emitted to `out/` (via `output: "export"`). Serve it with any static server:

```bash
npx serve out
```

## Project structure

```
ai-landing-page/
├── app/
│   ├── page.tsx        # Main landing page (hero, features, pricing, contact)
│   ├── layout.tsx      # Root layout, fonts, theme provider
│   ├── globals.css
│   ├── privacy/        # Privacy policy page
│   └── terms/          # Terms of service page
├── components/
│   ├── ui/             # navbar, pricing, bento-grid, spotlight, sparkles,
│   │                   # spline-scene, animated-gradient-background, …
│   └── theme-provider.tsx
├── hooks/              # Custom React hooks
├── lib/
│   └── utils.ts        # cn() class-name helper
├── public/             # Static assets and placeholders
└── next.config.mjs     # Next.js config (static export enabled)
```

## Environment variables

None required — the site is fully static with no backend. (If you connect a real contact form or CRM later, store keys in `.env.local`, which is already git-ignored.)

## Deployment

Statically exportable — deploy anywhere that serves static files:

- **Cloudflare Pages** — live at https://ai-landing-page.pages.dev
- Alternatively: GitHub Pages, Netlify, Vercel — just upload the `out/` directory after `pnpm build`.

No server, no database, no build-time secrets needed.

## Notes

- Generated with v0.app; the original v0 sync README has been replaced with this documentation.
- ESLint/TypeScript errors are ignored during builds (`next.config.mjs`) for frictionless static export.
- Placeholder images in `public/` can be swapped for real brand assets.

---

Built by Girish Lade — https://ladestack.in
