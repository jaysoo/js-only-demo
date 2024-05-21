This is a demo repo to show automatic dependency detection from `@mailchimp/experts` to `@mailchimp/wink`.

**Notes:**

1. Root `tsconfig.json` is generated with `npx tsc --init` (must add `typescript` package first).
2. `compilerOptions.paths` points directly to `index.js` files of the corresponding package. You can rename the entry point to the correct file.
3. Added JS plugin via `npx nx add @nx/js`, which is needed to locate TS/JS imports.
4. I've expanded the `^echo` dependency in `nx.json` to the full format in case that is more clear.

When you run `nx run @mailchimp/experts:echo --verbose` it'll also run the `echo` target of `@mailchimp/wink`.
