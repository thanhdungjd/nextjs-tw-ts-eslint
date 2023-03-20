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
  content: [
    "./app/**/*.{js,ts,jsx,tsx}",
    "./pages/**/*.{js,ts,jsx,tsx}",
    "./components/**/*.{js,ts,jsx,tsx}",
  ],
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
  <h1 className="text-red-500 block text-center border border-green-500 p-5  mx-auto mt-20 underline">
    cleaned up!
  </h1>
);
```

- run on dev mode

```bash
yarn && yarn dev
```
