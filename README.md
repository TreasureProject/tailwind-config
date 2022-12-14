# @treasure-project/tailwind-config

Treasure's resusable configuration preset. This can be very useful for teams that manage multiple Tailwind projects for the same brand where they want a single source of truth for colors, fonts, and other common customizations.

## Installation

Install `@treasure-project/tailwind-config` with npm (or yarn)

```bash
npm install -D @treasure-project/tailwind-config // yarn add @treasure-project/tailwind-config
```

In `tailwind.config.js`, add this line

```js
presets: [require('@treasure-project/tailwind-config')],
```

You will now be able to access all the colors, width, etc exported in `tailwind-config`.

If you also wish to import the fonts, add this to the root of your app

**!!Importing CSS files that reference other static assets don't work in remix yet. Until [this](https://github.com/remix-run/remix/issues/1153) is solved!!**

```js
import "@treasure-project/tailwind-config/fonts.css";
```

Now you can use the font via tailwind or from a stylesheet like solved

```
body {
    font-family: "Whyte", sans-serif;
}
```

## License

[MIT](https://choosealicense.com/licenses/mit/)

## Authors

- [@jcheese1](https://www.github.com/jcheese1)
