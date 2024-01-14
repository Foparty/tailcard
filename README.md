# Configuración prettier / eslint / order tailwind

## this is a template to start a new astro project with NOTHING but prettier / eslint / and tailwind configured

`bun create astro@latest .`

## prettier

https://docs.astro.build/en/editor-setup/#prettier

`bun install --save-dev prettier prettier-plugin-astro`

## eslint

https://ota-meshi.github.io/eslint-plugin-astro/user-guide/

`bun install --save-dev eslint eslint-plugin-astro`

then create a `.eslintrc.*`

and for example for cjs:

```
module.exports = {
  // ...
  extends: [
    // ...
    "plugin:astro/recommended",
  ],
  // ...
  overrides: [
    {
      // Define the configuration for `.astro` file.
      files: ["*.astro"],
      // Allows Astro components to be parsed.
      parser: "astro-eslint-parser",
      // Parse the script in `.astro` as TypeScript by adding the following configuration.
      // It's the setting you need when using TypeScript.
      parserOptions: {
        parser: "@typescript-eslint/parser",
        extraFileExtensions: [".astro"],
      },
      rules: {
        // override/add rules settings here, such as:
        // "astro/no-set-html-directive": "error"
      },
    },
    // ...
  ],
}
```

and cofigure it at will

## tailwind

https://tailwindcss.com/blog/automatic-class-sorting-with-prettier

`bunx astro add tailwind`

then

`bun install -D prettier prettier-plugin-tailwindcss`

and add this to .prettierrc

`{
  "plugins": ["prettier-plugin-tailwindcss"]
}`
# tailwindCard
