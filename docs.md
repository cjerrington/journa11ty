---
eleventyComputed: metadata.title
layout: layouts/home.njk
title: Docs
eleventyNavigation:
  key: Docs
  order: 2
---

## Design

This is a simple theme built with [11ty](https://www.11ty.dev/) and for CCS, [Pico](https://picocss.com/). I was wanting a basic site that was easy to setup so I could add notes and journal items.

The `pico` framework is real light weight and easy to configure. On this sites home page `pico` has it's own grid system and that is applied with a loop and shows 4 posts per row. If there are less than the 4 posts, they are still equally split for the width of the page.

A simple theme switcher is included and determines the light / dark theme based on user settings.

All posts can be found in the `posts` directory and you may use markdown or nunjucks files for your posts.

## Install

To begin using journa11ty you may Fork the repository and begin adding your posts and pages.

```shell
git clone https://github.com/cjerrington/journa11ty.git
```

Next install the packages

```shell
npm run install
```

There are some basic `run` scripts pre-written for you as well.

```json
"scripts": {
  "build": "npx @11ty/eleventy",
  "bench": "DEBUG=Eleventy:Benchmark* npx @11ty/eleventy",
  "watch": "npx @11ty/eleventy --watch",
  "serve": "npx @11ty/eleventy --serve",
  "start": "npx @11ty/eleventy --serve --watch",
  "dev": "npx @11ty/eleventy --serve",
  "debug": "DEBUG=* npx @11ty/eleventy"
}
```

## Using Pico

I decided in hopes to make it simpler for myself and others, to install picocss from npm. You can update the css theme file by updating the `.eleventy.js` copy function.

```js
eleventyConfig.addPassthroughCopy({"node_modules/@picocss/pico/css/pico.min.css": "css/pico.min.css"});
```

The documentation at [pico](https://picocss.com/) is easy to follow and make adjustments as needed.

## Using Prism for syntax highlighting

The `@11ty/eleventy-plugin-syntaxhighlight` is already installed along with PrismJS. Just like with Pico, the `npm` package is installed and you can choose your theme and update it in the copy function.

```js
eleventyConfig.addPassthroughCopy({"node_modules/prismjs/themes/prism-tomorrow.min.css": "css/prism-tomorrow.min.css"});
```

Check out [prismjs](https://prismjs.com/) for more details, but with 11ty we only need to supply the CSS file.

Current theme options:

- Default
- Dark
- Funky
- Okaidia
- Twilight
- Coy
- Solarized Light
- Tomorrow Night

## Custom CSS

There is a `custom.css` file that is passed in. This has a few site adjustments, but your own modifications are able to be added to this file as well.
