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