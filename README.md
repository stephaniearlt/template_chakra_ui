# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default tseslint.config({
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

- Replace `tseslint.configs.recommended` to `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`
- Optionally add `...tseslint.configs.stylisticTypeChecked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update the config:

```js
// eslint.config.js
import react from 'eslint-plugin-react'

export default tseslint.config({
  // Set the react version
  settings: { react: { version: '18.3' } },
  plugins: {
    // Add the react plugin
    react,
  },
  rules: {
    // other rules...
    // Enable its recommended rules
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```
## How to Get Started

1. Clone the repository: Clone this project to your local machine using the following command:

git clone https://github.com/your-username/your-repository.git

2. Navigate into the project folder: Change into the project directory:

cd your-repository

3. Install dependencies: Install all required dependencies with:

npm install

4. Start the development server: Launch the Vite development server:

npm run dev

You can then view the application at http://localhost:5173.

## Folder Structure

Here is the basic structure of the project:

/src
  /components
    /Demo          <-- Use this folder to verify everything is working properly.
  /assets
  App.tsx
  main.tsx
/vite.config.ts
/package.json
README.md

The /Demo folder contains basic components you can use to verify that everything is working as expected.

## Customization

You can begin developing your app by modifying or adding components in the src/components folder. Chakra UI is already configured, so you can start using its components directly in your application.

Good luck with your project! 🚀
