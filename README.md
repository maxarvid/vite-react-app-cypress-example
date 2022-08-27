# Vite React App with Cypress

Vite React application scaffolded using the Vite template.

```bash
$ yarn create vite --template react
```

With `start-server-and-test` and `cypress` development dependencies:
```bash
$ yarn add -D start-server-and-test cypress
```
NB, screenshots and videos are turned off in `cypress.config.js` and `devServer` is given a Vite-specific value for the bundler key:
```js
import { defineConfig } from "cypress";

export default defineConfig({
  component: {
    devServer: {
      framework: "react",
      bundler: "vite",
    },
  },
  e2e: {
    baseUrl: "http://localhost:5173",
    video: false,
    screenshotOnRunFailure: false,
  },
});
```
