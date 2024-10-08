# Turborepo starter for Next.js / NestJS

This is an starter of Turborepo using with Next.js and NestJS along with Prisma and Shadcn-ui for development.

## Installation

1. Clone the repository
```bash
git clone https://github.com/blt-Tech-Dev/Turborepo-Boilerplate-with-Next.js-and-NestJS.git
```

2. Install the dependencies
```bash
pnpm install
```

3. Create a `.env` file in the database package of the project and add the following environment variables.

```bash
DATABASE_URL="postgresql://username:password@localhost:5432/dbname"
```

4. Run the prisma commands to generate the prisma client and apply the migrations.

```bash
pnpm db:generate
```

5. Seed the database with the following command. (optional)

```bash
pnpm db:seed
```

6. Run the development server

```bash
pnpm run dev
```

7. Open the browser and navigate to `http://localhost:3000` to see the Next.js app and `http://localhost:3333` to see the NestJS app.

## What's inside?

This Turborepo includes the following packages/apps:

### Apps and Packages

    .
    ├── apps
    │   ├── api                       # NestJS app (https://nestjs.com).
    │   └── web                       # Next.js app (https://nextjs.org).
    └── packages
        ├── @repo/api                 # Shared `NestJS` resources.
        ├── @repo/eslint-config       # `eslint` configurations (includes `prettier`)
        ├── @repo/database            # Shared `Prisma` resources.
        ├── @repo/jest-config         # `jest` configurations
        ├── @repo/typescript-config   # `tsconfig.json`s used throughout the monorepo
        └── @repo/ui                  # Shareable stub React component library.

Each package and application are 100% [TypeScript](https://www.typescriptlang.org/) safe.

### Utilities

This `Turborepo` has some additional tools already set for you:

- [TypeScript](https://www.typescriptlang.org/) for static type-safety
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting
- [Jest](https://prettier.io) & [Playwright](https://playwright.dev/) for testing

### Commands

This `Turborepo` already configured useful commands for all your apps and packages.

#### Build

```bash
# Will build all the app & packages with the supported `build` script.
pnpm run build

# ℹ️ If you plan to only build apps individually,
# Please make sure you've built the packages first.
```

#### Develop

```bash
# Will run the development server for all the app & packages with the supported `dev` script.
pnpm run dev
```

#### Prisma

```bash
# Will run the prisma commands for the `api` app. can be used to generate the prisma client in the root of the project.
pnpm db:generate

# Using this command you can push the database schema to the database.
pnpm db:push

# If you want to open the prisma studio, you can use the following command.
pnpm db:studio

# If you have a new migration, you can run the following command to apply the migration. using in the `database` package.
pnpm db:migrate

# If you want to seed the database, you can use the following command.
pnpm db:seed
```

#### test

```bash
# Will launch a test suites for all the app & packages with the supported `test` script.
pnpm run test

# You can launch e2e testes with `test:e2e`
pnpm run test:e2e

# See `@repo/jest-config` to customize the behavior.
```

#### Lint

```bash
# Will lint all the app & packages with the supported `lint` script.
# See `@repo/eslint-config` to customize the behavior.
pnpm run lint
```

#### Format

```bash
# Will format all the supported `.ts,.js,json,.tsx,.jsx` files.
# See `@repo/eslint-config/prettier-base.js` to customize the behavior.
pnpm format
```

### Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```bash
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your Turborepo:

```bash
npx turbo link
```

## Useful Links

Learn more about the power of Turborepo:

- [Tasks](https://turbo.build/repo/docs/core-concepts/monorepos/running-tasks)
- [Caching](https://turbo.build/repo/docs/core-concepts/caching)
- [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching)
- [Filtering](https://turbo.build/repo/docs/core-concepts/monorepos/filtering)
- [Configuration Options](https://turbo.build/repo/docs/reference/configuration)
- [CLI Usage](https://turbo.build/repo/docs/reference/command-line-reference)

## To Do

- [x] Add Prisma to the project
- [x] Add Shadcn-ui to the project
- [x] Add Share Dto to the project
- [ ] [WIP] Make Dockerfile for the project
- [ ] Add Storybook to the project
