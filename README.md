# Basic Website Starter

A modern vanilla HTML/CSS/JS website

## About

This repository contains all of the files needed to begin a basic static HTML website build (aka “JAMstack”).

In this repository you'll find all of the files needed for a basic HTML website:

1. [index.html](index.html) contains all of the HTML code
2. [styles.css](styles.css) contains all of the CSS styles
3. [scripts.js](scripts.js) contains all of the JavaScript code

It also includes two icons, [favicon.ico](favicon.ico) and [apple-touch-icon.png](apple-touch-icon.png) which, as long as they're named these particular names and present in the root folder of your website will be found and used automatically - no need for adding anything to our HTML as long as these two files are present.</p>

## Why

### The HTML

- `<!DOCTYPE html>` is required at the start of any HTML document to let the browser know that what follows is HTML (and not some other language like XML, or SVG, etc)

- `<meta charset=utf-8>` is required to set the character encoding of the file so we can use special characters without needing to encode as many things. You not only want this present, but ideally as early in the document as possible so you can use special characters right away

- `<meta name=viewport content="width=device-width, initial-scale=1">` this isn't strictly required, but it's a common way browsers configure the default viewport scaling on mobile devices. This meta tags makes it normal and appear at its natural size, rather than behaving like a desktop site scaled down to fit a smaller device

- every HTML document needs a `<title>`

- I've added the CSS stylesheet here via a `<link>` with the `rel=stylesheet` attribute so the browser knows it's a CSS stylesheet

- I've added theJavaScript file here with a `<script>` tag using the `type=module` attribute which tells the browser that the JavaScript file is an ES module. This is beneficial for a few reasons:

 - - It won't execute the JS before the document is finished loading so you don't need to worry about adding the `<script>` before the closing `</body>` tag or add event listeners

 - - It will run at the right time. Also all ES modules are `"use strict"` by default and this strict mode helps prevent many types of errors that are hard to debug from even happening

 - - Lastly, by being an ES module it's very easy to use `import` to import functions and values from other ES modules in a safe way

 ## The CSS

- `box-sizing: border-box;` sets a nicer box-model for computing the size of elements

- `text-rendering`, `-webkit-font-smoothing`, `-moz-osx-font-smoothing`, `font-kerning` these properties all configure better default font rendering in all browsers and this particular set of properties seems to help make fonts look consistent across different browsers and operating systems

- `-webkit-text-size-adjust: 100%;` this ensures that if viewed on a mobile device and rotated between portrait and landscape mode, the page will remain the same scale, rather than 'zooming in' when rotated to landscape mode to fill the width of the screen without changing the aspect ratio of the page being viewed