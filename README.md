## Install

This module is standard in all P'unk Avenue apostrophe projects. It provides warnings of potential bugs and errors in your code. It is recommended for developers of all skill levels working with Apostrophe.

In the project root directory run:

```bash
npm install eslint eslint-plugin-promise eslint-plugin-standard eslint-plugin-react eslint-config-standard eslint-config-punkave --save-dev
```

Also, add the following to `.eslintrc` in the root directory:

```json
{
  "extends": "punkave"
}
```

## Editors

If you're using Atom as your editor you can install the [ESLint plugin](https://atom.io/packages/linter-eslint), which provides an interface for ESLint and this configuration. [VSCode has similar features](https://github.com/Microsoft/vscode-eslint), this plugin may be installed in your editor already.

## Running it manually

Once you have installed all of the required npm packages and added your `.eslintrc` file, you can manually run:

```
npx eslint .
```

Some warnings, such as those about whitespace, can be fixed automatically:

```
npx eslint . --fix
```

## Making it mandatory: adding eslint to your tests

You can add it to the `test` property in `package.json`, like this:

```
"test": "mocha && eslint .",
```

Then `npm test` will not pass unless eslint passes. Here we assume you also have `mocha` tests. But you could combine this with any test command, or have it as the only test command. `&&` means "do not continue unless the previous command succeeded."
