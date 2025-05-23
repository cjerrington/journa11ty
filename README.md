# journa11ty

A simple [11ty](https://www.11ty.dev/) blog, notes, journal site using [Pico](https://picocss.com/) for CSS.

I wanted something quick and easy to setup and get working for some personal notes, journal, etc. I decided to use `pico` for the CSS framework since it was lightweight and still looked good.

This is a pretty basic and simple start to any 11ty template allowing you some basic features:

- blog
- pages
- tags
- light/dark theme switch
- code syntax highlighting

## Todo

- add RSS feeds
- install and deploy instructions
- pagination for home page

## Customizations

Pico is installed with NPM so you can choose your CSS version and theme.

```js
eleventyConfig.addPassthroughCopy({"node_modules/@picocss/pico/css/pico.min.css": "css/pico.min.css"});
```

PrismJS for code syntax highlighting is also installed with NPM for you to choose your version and theme.

```js
eleventyConfig.addPassthroughCopy({"node_modules/prismjs/themes/prism-tomorrow.min.css": "css/prism-tomorrow.min.css"});
```

Within `_data\metadata.json` you have some config values you can set like the name of the site, description, etc.
