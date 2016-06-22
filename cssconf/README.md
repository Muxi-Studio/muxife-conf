# Muxi CSS Style Guide

## CSS 

### Formatting

+ 2 spaces for indentation.
+ When using multiple selectors in a rule declaration, give each selector its own line.
+ Use 0 instead of none.
+ Don't add unit after 0.
+ Sort properties in certain order.(More on that, checkout the `.csscomb.json` file)
+ Inner Spaces.(More on that, checkout the `.sass-lint.yml` file)
+ Empty line between blocks.
+ New line at end of the file.
+ Trailing semicolon.
+ Use double quote. 

### Naming

Use BEM like naming with dashes. BEM, or “Block-Element-Modifier”, is a naming convention for classes in HTML and CSS. 


```
.banner {

}

.banner-container {

}

.banner-container-nav {

}
```

### ID Selector

Do not use ID selectors. While it is possible to select elements by ID in CSS, it should generally be considered an anti-pattern. ID selectors introduce an unnecessarily high level of [specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity) to your rule declarations, and they are not reusable.

For more on this subject, read [CSS Wizardry's article](http://csswizardry.com/2014/07/hacks-for-dealing-with-specificity/) on dealing with specificity.

### JavaScript hooks

Avoid binding to the same class in both your CSS and JavaScript. Conflating the two often leads to, at a minimum, time wasted during refactoring when a developer must cross-reference each class they are changing, and at its worst, developers being afraid to make changes for fear of breaking functionality.

We recommend creating JavaScript-specific classes to bind to, prefixed with `.js-`:

```
<button class="btn btn-primary js-request-to-book">Request to Book</button>

```

## SCSS

### Nesting

Max depth 2.

### Colors

+ No Color Literals
+ No Color Keyword

Color should be used as variable. Except perhaps white and black. Chances are a color isn't one-off, and even if you think it is, once it's in a variable you might see uses for it elsewhere. Variations on that color can often be handled by the Sass color functions like lighten() and darken() - which make updating colors easier (change in one place, whole color scheme updates).

#### Bad

````
.foo {
  background-color: #fff;
}
````

#### Good

````
$white: #fff;

.foo {
  background-color: $white;
}
````


## Credits

This style guide is heavily base on [Airbnb's css style guide](https://github.com/airbnb/css).

## Links

+ [Sass Style Guide](https://css-tricks.com/sass-style-guide/)



