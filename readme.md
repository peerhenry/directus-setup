# Directus Setup

This is a template project to get started with a custom Directus application. It runs Directus locally and offers support for maintaining migrations as well as extensions. The setup is based on https://www.createdirectusapp.com/.

## Running locally

```
yarn dev
```

This will execute in order:

- create the docker container for Postgres if it does not exist
- bootstrap Directus
- apply the schema from `directus-app/schema.yml`
- start the Directus application

## Exporting database schema

```
yarn dump
```

It will be exported to `schema.yml`

## Generating types

To generate the types for the extension, run:

```
directus models snapshot ../directus-extension-example/src/models.d.ts
```

This should generate the file `directus-extension-example/src/models.d.ts`.

### Automating type generation

To make it part of the `dump` command, add this to the `scripts` section of `directus-app/package.json`:

```
"dump:models": "directus models snapshot ../directus-extension-example/src/models.d.ts"
```