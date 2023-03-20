# READ ME

```bash
yarn create next-app nextjs-tw-ts-eslint
```

1. Clean up the code

## Install tailwindcss

- install tailwindcss

```bash
yarn add -D tailwindcss postcss autoprefixer
yarn tailwindcss init -p
```

- the post.config.js file will be created automatically

```js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
};
```

- tailwind.config.js

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['./app/**/*.{js,ts,jsx,tsx}', './pages/**/*.{js,ts,jsx,tsx}', './components/**/*.{js,ts,jsx,tsx}'],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

- globals.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

- index.tsx

```tsx
return (
  <h1 className="mx-auto mt-20 block border border-green-500 p-5  text-center text-red-500 underline">cleaned up!</h1>
);
```

- run on dev mode

```bash
yarn && yarn dev
```

## Install eslint

- install eslint:

```json
{
  // package.json

  // Copilot suggest
  "eslint": "^7.32.0",
  "eslint-config-next": "^11.1.2",
  "eslint-plugin-css-modules": "^3.9.0",
  "eslint-plugin-import": "^2.24.2",
  "eslint-plugin-jsx-a11y": "^6.4.1",
  "eslint-plugin-react": "^7.26.1",
  "eslint-plugin-react-hooks": "^4.2.0",
  "eslint-plugin-tailwindcss": "^1.4.0",
  "prettier": "^2.4.1",
  "prettier-plugin-sort-class-names": "^3.0.1",
  "prettier-plugin-tailwindcss": "^0.1.13",

  // Rent config
  "eslint": "7.32.0",
  "eslint-config-next": "11.1.2",
  "eslint-plugin-css-modules": "^2.11.0",
  "eslint-plugin-tailwindcss": "^3.6.0"
}
```

```bash
yarn add -D eslint eslint-config-next eslint-plugin-css-modules eslint-plugin-tailwindcss
# eslint-config-next? dont have in the config: reslintrc.json ? does need to install?
```

- .eslintrc.json

```js
{
  "extends": [
    "next/core-web-vitals",
    "plugin:tailwindcss/recommended",
    "plugin:css-modules/recommended"
  ],
  "plugins": ["tailwindcss","css-modules"]
}
```

<!--
Sau khi Cài eslint: đã thấy cảnh báo về class name của tailwindcss, nhưng không tự sửa được, cần cài thêm prettier để tự sửa. (predict & copilot suggest)
 -->

- install prettier, prettier-plugin-tailwindcss, prettier-plugin-sort-class-names
- postcss-nested(?)

```json
{
  // package.json
  "prettier": "^2.4.1",
  "prettier-plugin-sort-class-names": "^3.0.1",
  "prettier-plugin-tailwindcss": "^0.1.13"
}
```

```bash
yarn add -D prettier prettier-plugin-tailwindcss prettier-plugin-sort-class-names postcss-import
# yarn add postcss-nested
```

- .prettierrc.js

<!-- Rent config -->

```js
// prettier.config.js or .prettierrc.js
module.exports = {
  trailingComma: 'es5',
  tabWidth: 2,
  semi: true,
  singleQuote: true,
  bracketSameLine: true,
  printWidth: 120,
  plugins: [require('prettier-plugin-tailwindcss')],
};
```
