postcss-brunch
==============

Adds [PostCSS](https://github.com/ai/postcss) support to [brunch](https://github.com/brunch/brunch)


## Install

	npm install --save-dev postcss-brunch

## Add plugins

Add all plugins you want to use with PostCSS in your `package.json` file too. For example, here we add [Autoprefixer](https://github.com/ai/autoprefixer) and [CSS Wring](https://github.com/hail2u/node-csswring).

```javascript
{
  "postcss-brunch": "^2.0",
  "autoprefixer": "^6.3",
  "csswring": "^5.1"
}
```

Or, use `npm install --save-dev <plugin>` to get latest version in package.json.

Then, configure `postcss-brunch` in the `plugins` section of your `brunch-config` file, like so:

```javascript
plugins: {
  postcss: {
    processors: [
      require('autoprefixer')(['last 8 versions']),
      require('csswring')
    ]
  }
}
```

You can add as many processors as you want. CSS will be parsed only once. See [PostCSS](https://github.com/ai/postcss) and each plugins docs.

## License

MIT
