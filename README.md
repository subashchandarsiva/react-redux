# Starter Kit for Building Applications in React and Redux

Based on [Cory House's Pluralsight course](http://www.pluralsight.com/author/cory-house).

## Development

Use Node.js 22 or newer:

```sh
npm ci
npm start
```

Open http://127.0.0.1:3000. The webpack 5 development server binds to the local
loopback address with host checking enabled. The mock JSON API runs on port 3001.
Each npm start regenerates its mock database from tools/mockData.js.
Stop both processes with Ctrl+C.

## Build

Run npm run build to generate production assets in build/. The bundled API URL
is http://localhost:3001; this build is not configured for a hosted production
backend. Build output, installed dependencies, and the generated mock database
are excluded from Git.

ESLint remains available through:

```sh
NODE_ENV=development npx --no-install eslint src tools webpack.config.dev.js
```

It is no longer run through the removed webpack 4 loader. There is no
application unit test suite in this repository.

See [MAINTENANCE.md](MAINTENANCE.md) for validation and dependency update policy.
