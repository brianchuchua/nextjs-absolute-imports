# Next.js Absolute Imports Example

This is a Create Next App (https://nextjs.org/docs/api-reference/create-next-app) with absolute imports configured.

See https://nextjs.org/docs/advanced-features/module-path-aliases for more details.

I was running into issues adding this to existing projects, so created this repo to isolate the issue.

## How To Set Up Absolute Imports

Just add the following to `tsconfig.json`:

```
  "baseUrl": ".",
  "paths": {
    "@app/features/*": ["features/*"]
  }
```

And then restart VS Code.

## Issues

While the absolute imports worked immediately, VS Code was reporting the following:

`Cannot find module '@app/features/bananas' or its corresponding type declarations.ts(2307)`

I tried to go through https://stackoverflow.com/questions/55198502/using-eslint-with-typescript-unable-to-resolve-path-to-module/56696478

... but all that was needed was to restart VS Code.