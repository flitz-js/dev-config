[![npm](https://img.shields.io/npm/v/@flitz/body.svg)](https://www.npmjs.com/package/@flitz/body)

# @flitz/dev-config

Shared [ESLint](http://eslint.org/docs/developer-guide/shareable-configs.html) and [tsconfig.json](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) files for [flitz](https://github.com/flitz-js/flitz).

![meme](https://raw.githubusercontent.com/flitz-js/dev-config/master/assets/meme.jpg)

## Install

Run

```bash
npm install --save-dev eslint @flitz/dev-config
```

from the folder, where your `package.json` is stored.

## Usage

### ESLint

Once the `@flitz/dev-config` package is installed, you can use it by specifying `@flitz/dev-config` in the [`extends`](http://eslint.org/docs/user-guide/configuring#extending-configuration-files) section of your [ESLint configuration](http://eslint.org/docs/user-guide/configuring).

Create a `.eslintrc.js` file in the root folder of your project and use the following skeleton:

```js
module.exports = {
  "extends": "@flitz/dev-config",
  "rules": {
    // Additional, per-project rules...
  }
}
```

As optional feature, you can add script entry, called `lint` e.g., to your `package.json`:

```json
{
    "scripts": {
        "lint": "eslint -c .eslintrc.js --ext .ts <mySrcFolder>"
    }
}
```

### tsconfig.json

```json
{
  "extends": "@flitz/dev-config",
  "compilerOptions": {
  }
}
```

You can overwrite any [compiler options](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html).

## License

MIT © [Marcel Kloubert](https://github.com/mkloubert)
