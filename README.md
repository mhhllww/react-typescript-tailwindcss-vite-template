# React + TypeScript + Tailwindcss + Vite

This template provides a minimal setup to get **React** working in Vite with **ESLint** and **Prettier** rules.

Currently, ESLint and Prettier are configured to make it convenient for you to work with the **FSD** architecture.

You can change ESLint config for yourself removing FSD plugins:

```js
{
  "extends": [
    "eslint:recommended",
    "plugin:prettier/recommended",
    "plugin:@typescript-eslint/recommended",
    "@feature-sliced/eslint-config/rules/import-order",
    "@feature-sliced/eslint-config/rules/layers-slices",
    "@feature-sliced/eslint-config/rules/public-api/lite"
  ],
  "plugins": [
    "@typescript-eslint"
  ],
  "parser": "@typescript-eslint/parser",
  "settings": {
    "import/resolver": {
      "typescript": {
        "alwaysTryTypes": true
      }
    }
  }
}
```

Also, you can customize Prettier config as you like:

```js
{
  "trailingComma": "es5",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": true,
  "jsxSingleQuote": true,
  "bracketSameLine": true,
  "endOfLine": "auto",
  "importOrder": [
    "<THIRD_PARTY_MODULES>",
    "^@/pages/(.*)$",
    "^@/widgets/(.*)$",
    "^@/features/(.*)$",
    "^@/entities/(.*)$",
    "^@/shared/(.*)$",
    "^../(.*)",
    "^./(.*)",
    "(.css)$"
  ],
  "importOrderSeparation": true,
  "importOrderSortSpecifiers": true,
  "plugins": [
    "@trivago/prettier-plugin-sort-imports"
  ]
}
```
