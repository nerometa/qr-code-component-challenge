# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

So I accepted and finished this challenge the very same day. That's how easy it is for me. I will explain how this come to life.

### Links

- [Solution URl](https://www.frontendmentor.io/solutions/solution-qr-code-component-using-scss-and-bootstrap-Cc2CRBOgdy))
- [Live Site URL](https://nerometa.github.io/qr-code-component-challenge/))

## My process

### Built with

- HTML
- [SCSS](https://sass-lang.com/)
- [Bootstrap](https://getbootstrap.com/)

With SCSS and Bootstrap, this project maybe a little bit overkill, but I want to do it fast and efficient and these guys delivers.

### What I learned

In this design, centering a container or `<div>` in the middle of the page is a key here. This is how I made it with Bootstrap classes.

```html
<div
  class="attribution container d-flex flex-column justify-content-center align-items-center my-5 min-vh-100"
></div>
```

First of all, we need `min-vh-100` / `min-height: 100vh` to make sure that we can center our item, otherwise it will still be stuck on the top of the page even when you justify and align it already.

Since we only need to center one item and not multiple items, we will use `d-flex` class or `display: flex` here to not overcomplicated things.

Next, `justify-content-center` / `justify-content: center` will center our item _horizontally_. We use `align-items-center` / `align-items: center` to center our flex item _vertically_.

Then `my-5` for some top and bottom spaces. In case you didn't know, it's margin along the y-axis, so in vanilla CSS we can use `margin-top` and `margin-bottom`. More modern solution would be `margin-block`

---

About working with SCSS, you can have one main .scss file and other files can be partial (if I remember correctly). These files start with \_ in their name and they will not compile when you run a command or use Sass Watcher to compile it. I typically use partials to store variables and some reusable CSS codes, like CSS reset code snippets.

Then, you wanna use it in the main SCSS file by using `@use` follow by your partial path.

This is how I import it:

```scss
@use "reset";
@use "variables" as *;
```

Notice how those files don't need file extensions when you import them. Partials that got variables like this:

```scss
// Colors
$white: hsl(0, 0%, 100%);
$light-gray: hsl(212, 45%, 89%);
$grayish-blue: hsl(220, 15%, 55%);
$dark-blue: hsl(218, 44%, 22%);
```

They got namespace when importing, such as `colors.$white` if you `@use` it like this

```scss
@use "variables" as colors;
```

That's why I use `*` to not having to put namespaces whenever I want to use variables.

### Useful resources

- [A Modern CSS Reset](https://piccalil.li/blog/a-modern-css-reset/) - This helped me resets CSS values, like remove that body margin so you can apply truly full background color.
- [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=glenn2223.live-sass) - If you use Visual Studio Code, this is really helpful when you use Sass/SCSS. If you still have an extension by Ritwick Dey by the same name, switch to this one because the Ritwick Dey one is not maintained anymore.

## Author

- Website - [nerometa](https://github.com/nerometa/)
- Frontend Mentor - [@nerometa](https://www.frontendmentor.io/profile/nerometa)
