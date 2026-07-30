# Capell

Capell is a Laravel and Filament CMS platform. The organization is split into a small number of source monorepos, generated package split repositories, sites, demos, and operational tooling.

## Canonical source repositories

| Repository | Purpose |
| --- | --- |
| [`capell`](https://github.com/capell-app/capell) | Main Capell core CMS monorepo. |
| [`capell-packages`](https://github.com/capell-app/capell-packages) | First-party package monorepo. |
| [`capell-app`](https://github.com/capell-app/capell-app) | Sales and marketing site. |
| [`capell-docs`](https://github.com/capell-app/capell-docs) | Documentation site. |
| [`capell-demo`](https://github.com/capell-app/capell-demo) | Demo site. |
| [`capell-ruby`](https://github.com/capell-app/capell-ruby) | Ruby demo site. |
| [`capell-server`](https://github.com/capell-app/capell-server) | Backup of server configuration. |

## Generated split repositories

`core`, `admin`, `frontend`, `marketplace`, and `installer` are generated from `capell` for Composer installs. Do not merge contributor PRs directly into those repositories.

Individual package repositories such as `address`, `blog`, `layout-builder`, and `theme-saas` are generated from `capell-packages`. They accept focused collaborator PRs, but maintainers merge the forwarded PR in `capell-packages`.

## Contribution flow

- Core changes go to `capell`.
- First-party package changes go to `capell-packages`.
- Split package PRs are forwarded automatically to `capell-packages` under `packages/<package>`.
- Split repositories are updated by the monorepo split workflows on release tags.