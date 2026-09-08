# Dependency Maintenance

## Update Policy

Dependabot checks every npm package directory weekly on Monday. Minor and patch
updates are grouped; major upgrades remain separate PRs. Each directory allows
up to five version-update PRs. The schedule takes effect after the configuration
is merged into the default branch. Automatic merging is not configured; review
updates and run the relevant checks before merging.

## September 8, 2026 Update

Updated webpack and its dev server to major version 5; refreshed React/Redux dependencies while retaining the application APIs. Removed unused scaffold dependencies, added a lockfile and production build, and restored dev-server host checking.

Validation: Production build passed with bundle-size warnings. Live checks passed for mock API reads, invalid request rejection, creation, and webpack dev-server HTML and bundle delivery.

The npm audit result for the updated lockfile is **0 critical, 0 high, 5 moderate**.
These counts include npm dependency propagation and are not directly comparable
to GitHub Dependabot advisory counts. Re-run npm audit for current results.

Five moderate findings remain. This update does not move every framework to its newest major version.
