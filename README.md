<div align="center">

<a href="https://www.jammeryhq.com" title="JammeryHQ" target="_blank">

  <img src="./jammeryhq.png" width="128" />
  
</a>

<p>
Fast-track your JAMstack development & learning
</p>
</div>

<hr />

# About this plugin

Gridsome Remark plugin to add css classes to any element

# Installation

```bash
npm install --save @jammeryhq/gridsome-remark-classes

# or

yarn add @jammeryhq/gridsome-remark-classes
```

## How to use

```js
//gridsome.config.js

module.exports = {

  plugins: [
    {
      use: '@gridsome/source-filesystem',
      options: {
        typeName: 'Blog',
        path: './content/blog/**/*.md',
      }
    }
  ],

  transformers : {
    remark : {
      plugins : [
        ['@jammeryhq/gridsome-remark-classes', {
          'heading[depth=1]': 'title',
          'heading[depth=2]': 'subtitle',
          'paragraph': 'text-normal font-serif'
        }]
      ]
    }
  }
}
```
## Documentation

You can find the complete documentation here: https://webstone.info/documentation/gridsome-remark-classes

## Credits

Inspired by [chrisg86/gatsby-remark-classes](https://github.com/chrisg86/gatsby-remark-classes)