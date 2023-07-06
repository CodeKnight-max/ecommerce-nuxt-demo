<p align="center">
  <a href="https://www.meilisearch.com/?utm_campaign=ecommerce-demo&utm_source=github&utm_medium=readme" target="_blank">
    <img src="https://github.com/meilisearch/meilisearch/blob/main/assets/logo.svg" alt="Meilisearch" width="200" height="200" />
  </a>
</p>

<h1 align="center">Meilisearch Nuxt 3 ecommerce demo</h1>

<h4 align="center">
  <a href="https://www.meilisearch.com/?utm_campaign=ecommerce-demo&utm_source=github&utm_medium=readme">Website</a> |
  <a href="https://www.meilisearch.com/pricing?utm_campaign=ecommerce-demo&utm_source=github&utm_medium=readme">Meilisearch Cloud</a> |
  <a href="https://blog.meilisearch.com/?utm_campaign=ecommerce-demo&utm_source=github&utm_medium=readme">Blog</a> |
  <a href="https://docs.meilisearch.com/?utm_campaign=ecommerce-demo&utm_source=github&utm_medium=readme">Documentation</a> |
  <a href="https://discord.meilisearch.com/?utm_campaign=ecommerce-demo&utm_source=github&utm_medium=readme">Discord</a>
</h4>

<p align="center">
  <a href="https://github.com/meilisearch/demo-movies/blob/main/LICENCE"><img src="https://img.shields.io/badge/license-MIT-informational" alt="License"></a>
</p>
<br/>

## 💪 Looking to build this yourself?

Read our [Step by step guide to adding site search to your Nuxt ecommerce](https://blog.meilisearch.com/nuxt-ecommerce-search-guide/?utm_campaign=ecommerce-demo&utm_source=github&utm_medium=readme)!

## 🧰 Stack

This project requires:

- [Node 18](https://nodejs.org/)
- [Yarn](https://classic.yarnpkg.com/) — Node.js packages manager
- [Nuxt 3](https://nuxt.com) — Web application framework based on [Vue 3](https://vuejs.org/)
- [Meilisearch](https://meilisearch.com/?utm_campaign=ecommerce-demo&utm_source=github&utm_medium=readme) — Fast, relevant search engine

## 🛠️ Setup

### Dependencies

> **Warning**
> Ensure that you are using a Node version compatible with the one in `.nvmrc`.

Install the dependencies with Yarn:

```bash
yarn install
```

### Environment

Environment variables should hold your Meilisearch database credentials. The easiest way to launch a database is to [create a free project](https://cloud.meilisearch.com/) on Meilisearch Cloud. Alternatively, you can read [local installation](https://docs.meilisearch.com/learn/getting_started/installation.html#local-installation?utm_campaign=ecommerce-demo&utm_source=github&utm_medium=readme) documentation for self-hosted options.

This project loads environment variables from an `.env` file. You can duplicate the existing `.env.example` file and rename it as `.env`. Update the content of the file to match your credentials.

```bash
# .env

# Meilisearch configuration
MEILISEARCH_HOST="use the Database URL here"
MEILISEARCH_ADMIN_API_KEY="use the Default Admin API Key here"
MEILISEARCH_SEARCH_API_KEY="use the Default Search API Key here"

# Image optimization configuration
TWICPICS_DOMAIN=https://meilisearch-ecommerce.twic.pics
STORYBOOK_TWICPICS_DOMAIN=https://meilisearch-ecommerce.twic.pics
```

> This application uses [TwicPics](https://twicpics.com/) to deliver optimized images. You don’t need to update the related environment variables. 

### Database

Run the setup script to configure and seed your Meilisearch instance:

```bash
yarn setup
```

## 🧑‍💻 Development

> **Note**
> Make sure to complete instructions from the Setup section before running the server.

Start the development server on http://localhost:3000

```bash
yarn dev
```

## 🚀 Deployment

Build the application for production:

```bash
yarn build
```

Locally preview production build:

```bash
yarn preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.

## ✨ Storybook

This project uses [Storybook v7](https://storybook.js.org/) to document components. The `vite.config.ts` is used by Storybook to enable auto-imports and path aliases.

Open Storybook by running:

```bash
yarn storybook
```

> Output files `auto-imports.d.ts` and `components.d.ts` are auto-generated and *should not* be updated manually. You can commit them into source control.

