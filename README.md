## Install

This module is for advanced users looking for a shareable configuration across projects for ESLint.

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
