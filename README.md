# [sv](https://svelte.dev/docs/cli/overview) community add-on: [@msw/sveltekit](https://github.com/mswjs/sveltekit)

> [!IMPORTANT]
> Svelte maintainers have not reviewed community add-ons for malicious code. Use at your discretion.

## Usage

```shell
# in an existing sveltekit project
npx sv add @msw/sveltekit

# create a new project with msw
npx sv create --add @msw/sveltekit
```

## What you get

- `msw` added as a dev dependency.
- `src/msw/handlers.ts` or `src/msw/handlers.js` with shared request handlers.
- Optional browser setup in `src/msw/browser` and `src/hooks.client`.
- Optional Node setup in `src/msw/node` and `src/hooks.server`.
- Browser worker configuration in `package.json`.

## Options

### `environments`

Choose where MSW should run. This is a multiselect option.

Default: `browser,node`

```shell
npx sv add @msw="environments:browser,node"
```

## Browser worker

If you enable browser mocking, generate the service worker after installing dependencies:

```shell
npx msw init static --save
```
