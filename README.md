![Gutenberg](http://i.imgur.com/NlGJI3v.png)

> Modern framework to print correctly

[![npm (scoped)](https://img.shields.io/npm/v/gutenberg-css.svg?style=flat-square)](https://www.npmjs.com/package/gutenberg-css)

# How to use

Simply include the right stylesheet(s) in your html an load it only for a printer.
Gutenberg.css is the base stylesheet but there is themes available in the `themes` folder.

Example with Gutenberg and "old style" theme :

```HTML
<link rel="stylesheet" href="dist/gutenberg.css" media="print">
<link rel="stylesheet" href="dist/themes/oldstyle.css" media="print"> <!-- optional -->
```

![comparison](https://i.imgur.com/tL5cHhn.png)

> Comparison between standard print (left) and Gutenberg (middle, Modern style and right, Old style)

## CDN

You can also use the unpkg service as a *CDN*.

```HTML
<link rel="stylesheet" href="https://unpkg.com/gutenberg-css@0.3.0" media="print">
<link rel="stylesheet" href="https://unpkg.com/gutenberg-css@0.3.0/dist/themes/oldstyle.min.css" media="print">
```


# What does the framework do ?

### Hide elements

To hide elements to be printed you can simply add the class `no-print`.

### Force break page

Gutenberg provide to way break page, the class `page-break` will for to break before and `page-break-after` to break after.

Example:

```HTML
<!-- The title will be on a new page -->
<h1 class="page-break">My title</h1>

<p class="page-break-after">I will break after this paragraph</p>
<!-- Break here, the next paragraph will be on a new page -->
<p>I am on a new page</p>
```

### Not reformat links or acronym

If you do not want to reformat the links, acronym or abbreviation to show the full url or title, you
can use the class `no-reformat`.

### Force to print background

To force backgrounds to be printed (can be useful when you "print" a pdf), add this CSS (compatible with Safari and Chrome) :

```CSS
-webkit-print-color-adjust: exact;
        print-color-adjust: exact;
```

## Dev

 1. `npm install` to install dependencies
 2. `gulp watch` to "watch" the scss folder and compile to css
