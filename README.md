# Useful stuff

---

## Links

**Website:** https://www.electronjs.org/
**Documentation:** https://www.electronjs.org/docs/latest/
**Examples:** https://www.electronjs.org/docs/latest/tutorial/examples

## Packages

### yarn

-   **devDependencies:** `yarn add electron electron-builder concurrently wait-on -D`
-   **dependencies:** `yarn add cross-env electron-is-dev`

### npm

-   **devDependencies** `npm install --save-dev electron electron-builder concurrently wait-on`
-   **dependencies** `npm install cross-env electron-is-dev`

## Custom scripts

I prefixed the "original" react scripts with "react-" and added custom ones
You can create your own scripts with other names ofc

```
{
    scripts": {
        "scripts": {
        "react-start": "react-scripts start",
        "react-build": "react-scripts build",
        "react-test": "react-scripts test",
        "react-eject": "react-scripts eject",
        "electron-build": "electron-builder",
        "build": "npm run react-build && npm run electron-build",
        "start": "concurrently \"cross-env BROWSER=none npm run react-start\" \"wait-on http://localhost:3000 && electron .\""
    },
      },
  }
```
