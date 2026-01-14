## Database and Drizzle Rules

The `db` folder is the single source of truth for database definitions.

### Structure

- `db/index.ts` handles database connection
- `db/schema.ts` contains:
  - Drizzle table definitions
  - Zod schemas generated via drizzle-zod

### Rules

- Table definitions and Zod schemas live together to stay in sync
- Services may import directly from `db/schema.ts`
- Do not define Zod schemas elsewhere
