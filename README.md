# bug-sveltekit-external-link

For issue: https://github.com/sveltejs/kit/issues/3402

## To Reproduce

Run `npm run build`.

## The Setup

To create this reproduction, I did:

```
npm init svelte@next bug-sveltekit-external-link
cd bug-sveltekit-external-link
```

The `package.json` was updated with these:

```
  "devDependencies": {
    "@sveltejs/adapter-static": "^1.0.0-next.26",
    "@sveltejs/kit": "^1.0.0-next.229",
    "svelte": "^3.46.1"
  },

```

Did `npm install`.


Then the `app.html` file was edited, adding a single stylesheet `<link>` served externally to
the `<head>` section. E.g.:

```
<link rel="stylesheet" href="/webjars/mdi__font/5.8.55/css/materialdesignicons.min.css">
```

Then build fails with `npm run build`.

