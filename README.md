# MCP Bookmark Manager

A simple and efficient bookmark manager built with Next.js, Prisma, and Clerk. It lets you securely manage, organize, and search bookmarks with authentication support and an easy-to-extend architecture. Ideal for personal use or integration with MCP workflows.

## Requirements

* Node.js 18+
* npm or pnpm

## Environment Variables

Create a `.env` file in the project root with the following keys:

```
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=<your_clerk_publishable_key>
CLERK_SECRET_KEY=<your_clerk_secret_key>
DATABASE_URL=<your_database_url>
```

## Setup

```bash
git clone https://github.com/danish0511/MCP-bookmark-manager.git
cd MCP-bookmark-manager
npm install
```

## Database & Prisma

```bash
# Generate Prisma client
npx prisma generate

# Apply migrations (creates DB if needed)
npx prisma migrate dev --name init
```

## Development

```bash
npm run dev
```

The app will start on [http://localhost:3000](http://localhost:3000).

## Build

```bash
npm run build
npm start
```

## Project Structure (brief)

```
prisma/          # Prisma schema & migrations
src/             # Application source
  app/           # Next.js App Router routes and API
  components/    # UI components
  lib/           # Utilities (e.g., db client)
  hooks/         # Custom React hooks
  types/         # Shared TypeScript types
  middleware/    # API and auth middlewares
```

## Notes

* Ensure all three environment variables are set before running.
* For local development you can use SQLite via `DATABASE_URL="file:./dev.db"`.
