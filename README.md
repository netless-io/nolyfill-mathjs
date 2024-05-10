# @netless/nolyfill-mathjs

Helper package to nolyfill (invalidate) `mathjs` from `white-web-sdk`'s dependencies.

Because `mathjs` is used to render the legacy PPT. Using this package can be
helpful when you do not want to use legacy PPT and to include `mathjs` in your final bundle.

## Usage

Edit your `package.json`.

### NPM

https://docs.npmjs.com/cli/v10/configuring-npm/package-json#overrides

```js
{
  "overrides": {
    "white-web-sdk": {
      "mathjs": "npm:@netless/nolyfill-mathjs@0.1.0"
    }
  }
}
```

Then run `npm install`.

### PNPM

https://pnpm.io/package_json#pnpmoverrides

```js
{
  "pnpm": {
    "overrides": {
      "white-web-sdk>mathjs": "npm:@netless/nolyfill-mathjs@0.1.0"
    }
  }
}
```

Then run `pnpm install`.

### Yarn (v1)

https://classic.yarnpkg.com/lang/en/docs/selective-version-resolutions/#toc-how-to-use-it

```js
{
  "resolutions": {
    "white-web-sdk/mathjs": "npm:@netless/nolyfill-mathjs@0.1.0"
  }
}
```

Then run `yarn install`.

## License

MIT @ [netless](https://github.com/netless-io)
