# Nuxt Generate static site sample

## DIY Steps

1. initialize project
```bash
npx create-nuxt-app test-nuxt
```

2. install these package for cross-platform files.
```bash
npm i -D copyfiles rimraf
```

3. Edit npm script
```diff
scripts: {
  ...
+ "build-docs": "rimraf docs && npm run generate && copyfiles --up 1 \"dist/**/*\" \"docs/\"",
  ...
}

```

4. Run build setup below.
## Build Setup

``` bash
# install dependencies.
$ npm ci

# generate static project.
$ npm run build-docs

# serve and test your project.
$ npx serve docs/
```
