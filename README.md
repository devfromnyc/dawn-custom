# Dawn Custom

## Getting started

## Staying up to date with Dawn changes

Say you're building a new theme off Dawn but you still want to be able to pull in the latest changes, you can add a remote `upstream` pointing to this Dawn repository.

1. Navigate to your local theme folder.
2. Verify the list of remotes and validate that you have both an `origin` and `upstream`:

```sh
git remote -v
```

3. If you don't see an `upstream`, you can add one that points to Shopify's Dawn repository:

```sh
git remote add upstream https://github.com/Shopify/dawn.git
```

4. Pull in the latest Dawn changes into your repository:

```sh
git fetch upstream
git pull upstream main
```

## Developer tools

### Shopify CLI

[Shopify CLI](https://github.com/Shopify/shopify-cli) helps you build Shopify themes faster and is used to automate and enhance your local development workflow. It comes bundled with a suite of commands for developing Shopify themes—everything from working with themes on a Shopify store (e.g. creating, publishing, deleting themes) or launching a development server for local theme development.

You can follow this [quick start guide for theme developers](https://github.com/Shopify/shopify-cli#quick-start-guide-for-theme-developers) to get started.

### Continuous Integration

Dawn uses [GitHub Actions](https://github.com/features/actions) to maintain the quality of the theme. [This is a starting point](https://github.com/Shopify/dawn/blob/main/.github/workflows/ci.yml) and what we suggest to use in order to ensure you're building better themes. Feel free to build off of it!

#### Shopify/lighthouse-ci-action

We love fast websites! Which is why we created [Shopify/lighthouse-ci-action](https://github.com/Shopify/lighthouse-ci-action). This runs a series of [Google Lighthouse](https://developers.google.com/web/tools/lighthouse) audits for the home, product and collections pages on a store to ensure code that gets added doesn't degrade storefront performance over time.

#### Shopify/theme-check-action

Dawn runs [Theme Check](#Theme-Check) on every commit via [Shopify/theme-check-action](https://github.com/Shopify/theme-check-action).

## Contributing
