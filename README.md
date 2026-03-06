<div align="center">

# React + NestJS Starter

![React](https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**Production-ready fullstack monorepo starter with authentication, RBAC, and CI/CD out of the box.**

[Getting Started](#getting-started) · [Architecture](#architecture) · [Features](#features) · [Deployment](#deployment)

</div>

---

## Features

- **Frontend**: React 19 + Vite, TanStack Router, TanStack Query, Zustand, Tailwind CSS, Radix UI
- - **Backend**: NestJS + Fastify, Prisma ORM, PostgreSQL, JWT + Refresh tokens, RBAC
  - - **API**: REST endpoints + optional GraphQL (Apollo Server) with code generation
    - - **Auth**: Email/password, OAuth (Google, GitHub), 2FA (TOTP), password reset flow
      - - **DevOps**: Docker Compose, GitHub Actions CI/CD, Vercel/Railway deployment configs
        - - **Testing**: Jest + Testing Library, Jest + Supertest, Playwright E2E
          - - **DX**: ESLint, Prettier, Husky, lint-staged, conventional commits, path aliases
           
            - ## Architecture
           
            - ```
              react-nestjs-starter/
              ├── apps/
              │   ├── web/                  # React 19 + Vite frontend
              │   │   └── src/
              │   │       ├── components/   # Shared UI components
              │   │       ├── features/     # Feature-based modules
              │   │       ├── hooks/        # Custom React hooks
              │   │       ├── routes/       # TanStack Router pages
              │   │       └── stores/       # Zustand stores
              │   └── api/                  # NestJS backend
              │       └── src/
              │           ├── auth/         # JWT, OAuth, 2FA
              │           ├── users/        # User CRUD + RBAC
              │           ├── common/       # Guards, decorators, pipes
              │           └── prisma/       # Prisma service + migrations
              ├── packages/
              │   ├── shared/               # Shared types, validation (Zod)
              │   └── eslint-config/        # Shared ESLint config
              ├── docker-compose.yml
              ├── turbo.json
              └── .github/workflows/        # CI/CD pipelines
              ```

              ## Getting Started

              ```bash
              git clone https://github.com/mykhayloyuminov/react-nestjs-starter.git
              cd react-nestjs-starter
              pnpm install
              docker compose up -d
              pnpm db:migrate && pnpm db:seed
              pnpm dev
              ```

              Frontend: `http://localhost:3000` · API: `http://localhost:4000`

              ## Scripts

              | Command | Description |
              |---------|-------------|
              | `pnpm dev` | Start all apps in dev mode |
              | `pnpm build` | Build all apps |
              | `pnpm test` | Run unit tests |
              | `pnpm test:e2e` | Run Playwright E2E tests |
              | `pnpm db:migrate` | Run Prisma migrations |
              | `pnpm db:studio` | Open Prisma Studio |
              | `pnpm lint` | Lint all packages |

              ## Deployment

              **Vercel** (Frontend) · **Railway/Render** (Backend) · **Docker Compose** (Self-hosted)

              ## License

              MIT — see [LICENSE](LICENSE) for details.

              ---

              <div align="center">
              Built by <a href="https://github.com/mykhayloyuminov">Mykhaylo Yuminov</a>a> · <a href="https://complete-solution.eu">Complete Solution</a>a>
              </div>div>
