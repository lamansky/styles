# styles

`styles` is a small library of CSS rules I find myself using in most web development projects. It is packaged as a [Sass](https://sass-lang.com/) module.

## Installation and Usage

If you have [Node.js](https://nodejs.org/en/) installed, you can add this module to your project using npm:

```bash
npm i @lamansky/styles
```

Assuming you’re using [webpack](https://webpack.js.org/) for your project, include the module into your own Sass/SCSS stylesheet like so:

```scss
@use "~@lamansky/styles";
```

You can then add your own styles that make use of the mixins:

```scss
@use "~@lamansky/styles";

ul {
  @include styles.bare-list;
  padding: 1em;
}

nav .skip-link {
  @include styles.screen-reader-only;
  cursor: pointer;
}
```

This module includes two mixins:

* **bare-list**, which is used to strip `list-style`, `margin`, and `padding` from a `ul` or `ol` and its child `li` elements.
* **screen-reader-only**, which uses `clip` to hide text from a visual user agent but leave it accessible to screen reading software.

## Related

* [mq](https://github.com/lamansky/mq): A library of media query mixins for Sass.
