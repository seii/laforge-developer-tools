# Tweaks to LAFORGE Shima Simulator
[LAFORGE Optical](https://laforgeoptical.com) is making an impressive Augmented Reality pair of prescription glasses called [Shima](https://laforgeoptical.com/pages/meet-shima). They have released a [simulator]() for development purposes.

## Problem
Unfortunately, the version used as of this writing (February 19, 2018) only works on Google Chrome browsers due to its utilization of HTML5 Web Components. That's not a bad thing, and hopefully all browsers will be able to implement that standard soon. However, most browsers still need polyfills as the standard isn't widely implemented yet.

## Installation
- Clone this repository
- Run `npm install`
- Copy all `.js` files from `node_modules/@webcomponents/webcomponentsjs` into the `public/lib` folder
- Run `npm start`

(The copied files will allow the auto-loader component to choose which library is necessary based on browser capabilities.)

## Differences
- **Polyfill:** The [official Web Components site](https://www.webcomponents.org/) has already implemented polyfills, along with [instructions](https://www.webcomponents.org/polyfills) on how to use them. I have taken their advice and inserted the polyfill code and libraries into LAFORGE's existing simulator code.
- **Naming:** The current `package.json` file was not in conformance with npm's [package.json spec](https://docs.npmjs.com/files/package.json#name) due to something very simple, its name. The existing name had used capital letters and spaces, something that npm won't abide. I have shortened the name down to `laforge-developer-tools`, which is the same name but in all lowercase and using hyphens instead of spaces.

## Legacy information
The below snippet was already present in LAFORGE's `README.md`, and is preserved:

Shima Mock API Documentation
------------

The Mock API Documentation can be found on [doclets here](https://doclets.io/DoubleTap-Consulting/laforge-shima-api/master)
