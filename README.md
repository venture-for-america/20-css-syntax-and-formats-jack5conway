# CSS Syntax and Formats

## Overview

In this lesson we will do a quick review of CSS syntax and formating from the video lecture in the prior lesson.

## What's Covered in This Lesson 

1. Review CSS Syntax
2. Review Possible CSS Formats

### What Is The Purpose of CSS?

CSS stands for Cascading Style Sheet. Cascading because it can apply to multiple elements across many pages, and style sheet because it is a single body of code that adds style across the many pages it affects. We can imagine the HTML as the structure of a house, the brick and mortar, the walls, the ceilings, the roof. The CSS then paints the walls and arranges the furniture. It is the decorator that breathes color, typographic style, and positioning of elements among other things. It was created as an easier way to style our pages from a single location.

### Syntax

CSS has a unique syntax separate from HTML.

```css
p { 
  color: red;
}
```

In the code example above `p` is known as a selector; in this case it is selecting all paragraphs in the HTML pages linking to this CSS file. Selectors determine which elements will be affected by the styles we set. Following this in `{}` curly braces are declarations which are CSS rules that will style our selected element. Declarations are made up of a property shown here as `color` followed by a value shown here as `red`. Notice that we use a `:` colon to separate the property from its value. All declarations end in a `;` semicolon. Multiple declarations can be applied to the same selector as seen below. 

```css
p {
    color: red;
    font-weight: bold;
}
```
### Formats

CSS can appear in our code in three distinct formats: Inline, Internal, or External.

#### Inline

Inline CSS is written within a `style` attribute and only effects the single element that the attribute is included within.

```html
<p style="color:red;">Lorem ipsum</p>
```

#### Embedded

Embedded CSS is included typically within the `<head>` section of an HTML document within `<style>` elements. This only affects the elements selected across the particular page that it is included within.

```html
<style>
  p {
    color: red;
  }
</style>
```
#### External

External CSS is written inside an external and separate file that is then linked to from other HTML pages. This is the preferred format to use as it allows us to affect the style of many HTML pages site-wide from a single file. This has two components to make it work: our CSS must be written in its own `.css` file, and in our HTML file we must link to our CSS from our head section.

**css/style.css**

```css
p {
   color: red; 
}
```

**index.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="css/style.css">
  </head>
  <body>
    <p>Lorem ipsum</p>
  </body>
</html>
```

### Comments

To comment in CSS simply start with `/*` and end with `*/`

```css
/* this is a comment */

/* It can be single, 
   or multiple lines */
```

## Summary

- CSS allows us to style our HTML pages.
- CSS has three distinct formats, although external CSS is considered the best option for styling websites.
- Comments in CSS are written like `/* this */`.

## Resources

- [MDN - CSS Tutorials for Beginners](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started)
- [MDN - CSS Property Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

<p class='util--hide'>View <a href='https://learn.co/lessons/css-syntax-formats'>Syntax and Formats</a> on Learn.co and start learning to code for free.</p>
