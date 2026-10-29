# <Product name>

@.claude/agent-rules.md

## Overview

<What this product does and who uses it, in 3–5 sentences.>

## Repository layout

- `src/<Product>.Api/` – <ASP.NET Core API>
- `src/<Product>.Web/` – <Angular frontend>
- `tests/` – <unit and integration tests>

## Build, test and lint

Run all of these before every push. All must pass.

```bash
dotnet build --configuration Release
dotnet test --configuration Release --no-build
dotnet format --verify-no-changes

cd src/<Product>.Web
npm ci
npm run lint
npm test -- --watch=false
```

## Conventions

- <e.g. Minimal APIs grouped per feature under src/<Product>.Api/Features/>
- <e.g. Async all the way; no .Result or .Wait()>
- <e.g. New endpoints need an integration test in tests/<Product>.Api.Tests/>
- <e.g. Angular: standalone components, signals for state>

## Things to avoid

- <e.g. Do not touch generated clients in src/<Product>.Web/src/app/api/; regenerate them instead>
- <e.g. Database migrations need a human; describe the change and stop>
