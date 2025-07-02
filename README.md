# Medusa v2 Example: Product Reviews

This directory holds the code for the [Product Review Guide](https://docs.medusajs.com/resources/how-to-tutorials/tutorials/product-reviews).

You can either:

- [install and use it as a Medusa application](#installation);
- or [copy its source files into an existing Medusa application](#copy-into-existing-medusa-application).

## Prerequisites

- [Node.js v20+](https://nodejs.org/en/download)
- [Git CLI](https://git-scm.com/downaloads)
- [PostgreSQL](https://www.postgresql.org/download/)

## Installation

1. Clone the repository and change to the `product-review` directory:

```bash
yarn add @godscodes/medusa-product-reviews
```

2\. Add the plugin to the `plugins` array in `medusa-config.ts`:

```ts
module.exports = defineConfig({
  // ...
  plugins: [
    {
      resolve: "@godscodes/medusa-product-reviews",
      options: {}
    }
  ]
})
```


You'll find a "Reviews" page in the Medusa Admin.

## Copy into Existing Medusa Application

If you have an existing Medusa application, copy the following directories and files into your project:

- `src/admin`
- `src/api`
- `src/links`
- `src/modules/product-review`
- `src/workflows`

Then, add the Product Review Module to `medusa-config.ts`:

```ts
module.exports = defineConfig({
  // ...
  modules: [
    {
      resolve: "./src/modules/product-review",
    }
  ],
})
```

Finally, run migrations:

```bash
npx medusa db:migrate
```

## More Resources

- [Medusa Documentatin](https://docs.medusajs.com)
- [OpenAPI Spec file](https://res.cloudinary.com/dza7lstvk/raw/upload/v1741941475/OpenApi/product-reviews_jh8ohj.yaml): Can be imported into tools like Postman to view and send requests to this project's API routes.
