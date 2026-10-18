# Kusanya

A Kenyan thrift marketplace: photo-first shops, an item feed, in-app chat and ratings from real buyers. The pilot starts with Gikomba sellers, then opens to Instagram and TikTok sellers.

> Working name. Confirm the brand name before launch.

## Status
Pre-build. See `docs/SPEC.md` for the full specification and the build tracker for dates.

## Stack (planned)
- Next.js (App Router), TypeScript, Tailwind CSS
- PostgreSQL with Prisma
- Docker Compose on a Nairobi VPS, Caddy for HTTPS, Cloudflare in front

## Folders
| Folder | Purpose |
|---|---|
| `docs/` | Specification, decisions, changelog |
| `design/` | Figma exports and design tokens |
| `infra/` | Server config (Caddy), backup scripts |
| `prisma/` | Database schema and migrations |
| `scripts/` | Seed data and helper scripts |
| `src/` | The application code |
| `tests/` | Unit and end-to-end tests |
| `public/` | Static files and images |

## Local development (once Node and Docker are installed)
```
cp .env.example .env
docker compose up -d
npm install
npx prisma migrate dev
npm run dev
```
Local email is captured by Mailpit at http://localhost:8025.

## Rules
- Never commit `.env` or any secret.
- Commit small and often, with clear messages.
