# @treasure-project/tailwind-config

Treasure's resusable configuration preset. This can be very useful for teams that manage multiple Tailwind projects for the same brand where they want a single source of truth for colors, fonts, and other common customizations.

## Installation

Install `@treasure-project/tailwind-config` with npm (or yarn)

```bash
npm install -D @treasure-project/tailwind-config
# or
yarn add -D @treasure-project/tailwind-config
```

In `tailwind.config.js`, add this line

```js
presets: [require('@treasure-project/tailwind-config')],
```

You will now be able to access all the colors, width, etc exported in `tailwind-config`.

### Fonts

If you also wish to use the fonts, import them int he root of your app

#### General

```js
import "@treasure-project/tailwind-config/fonts.css";
```

#### Remix
```js
import fontStylesheet from "@treasure-project/tailwind-config/fonts.css";
import stylesheet from "~/tailwind.css";

export const links: LinksFunction = () => [
  { rel: "stylesheet", href: fontStylesheet },
  { rel: "stylesheet", href: stylesheet },
];
```

Now you can use the font via tailwind or from a stylesheet:

```css
body {
    font-family: "Whyte", sans-serif;
}
```

## License

[MIT](https://choosealicense.com/licenses/mit/)

## Authors

- [@jcheese1](https://www.github.com/jcheese1)
