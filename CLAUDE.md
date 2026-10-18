# Project instructions for Claude Code

Read `docs/SPEC.md` first. It is the full specification. Then read `prisma/schema.prisma`, which is the starting database design.

## Who you are working with
Abigail is a student building this solo, with some non-technical help from her sister. Explain decisions in plain language. Keep code readable.

## Working rules
- Work in small steps. After each step: run it, run the tests, then commit with a clear message.
- Before any big decision (database change, new library, security trade-off), explain the options in a few lines and ask.
- Do not add features that are not in the spec. Put ideas in `docs/DECISIONS.md` under "Version 1.1 ideas".
- Never hard-code secrets. Use environment variables and keep `.env.example` current.
- Keep `docs/CHANGELOG.md` and `docs/DECISIONS.md` updated (one line per decision and why).
- The project folder already contains files. When scaffolding Next.js, merge into the existing folder and do not delete or overwrite my files.

## Product rules that must not be broken
- There is no checkout, wallet or escrow in the MVP. The platform never holds money.
- There is no WhatsApp handoff. All chat happens on the site.
- Sign-in is Google or email one-time code. No passwords. No Apple sign-in.
- Light and dark mode must work from the start.
- Usernames are unique (case-insensitive). Users must be 18 or older.
- Ratings only after a conversation, once per buyer per seller.
- Mobile first, low data, pages under 3 seconds on slow 3G.
- Only usernames are public. Names, phone numbers, emails and dates of birth stay private.
