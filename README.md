# Warehouse

Monorepo for the Warehouse application.

The project is managed with [Bun](https://bun.com) workspaces and contains separate frontend, backend, and shared packages.

## Structure

```text
warehouse/
├── backend/    # NestJS backend
├── frontend/   # React + Vite frontend
├── shared/     # Shared TypeScript types
├── package.json
└── bun.lock
```

## Requirements

- [Bun](https://bun.com) 1.4+
- Node.js is not required for running the project directly with Bun.

## Installation

Install all workspace dependencies from the repository root:

```bash
bun install
```

Bun uses the root workspace configuration and manages dependencies for all packages.

## Development

Run the backend in development mode:

```bash
bun run backend:dev
```

Run the frontend:

```bash
bun run frontend:dev
```

## Build

Build the backend:

```bash
bun run backend:build
```

Build the frontend:

```bash
bun run frontend:build
```

## Other commands

### Backend

```bash
bun run backend:start
bun run backend:format
bun run backend:lint
bun run backend:test
```

### Frontend

```bash
bun run frontend:lint
bun run frontend:preview
```

## Workspaces

The repository uses Bun workspaces:

```json
{
  "workspaces": ["backend", "frontend", "shared"]
}
```

Workspace-specific commands can also be executed directly with Bun's `--filter` option:

```bash
bun --filter @warehouse/backend build
bun --filter @warehouse/backend start:dev
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
