# Bootstrap Scaffold

## Overview

Creates a new Bootstrap 4 project using git and npm.

Includes:

- A pipeline to compile, autoprefix, minify, and copy SCSS.
- An HTTP server for local development.
- A LiveReload server for local development.

## Installation

```bash
git clone git@github.com:jmooring/bootstrap-scaffold.git
cd my-project
npm install
npm start
```

The `npm start` command is an alias for `npm run watch`.

## Files and Directories

src/scss/main.scss
> This is the starting point for SCSS compilation. Import custom SCSS files as needed.

src/scss/_variables.scss
> Override existing Bootstrap variables, and add custom variables as needed.

src/scss/_shame.scss
> Hacks and other things we're not proud of. See <https://csswizardry.com/2013/04/shame-css>.

dist/
> Files created during the build process.

public/
> Root of website.

## Scripts

Run these scripts using npm:

```bash
npm run script-name
```

css:compile
> Compiles SCSS to CSS.

css:prefix
> Autoprefixes the CSS created by css:compile.

css:minify
> Minifies the CSS created by css:prefix.

css:copy
> Copies the CSS created by css:minify from dist/css/ to public/assets/css/.

css:build
> Sequentially calls css:compile, css:prefix, css:minify, and css:copy.

css:watch
> Recursively watches for changes in src/scss, and runs css:build when changes are detected.

livereload
> Starts the LiveReload server.

http-server
> Starts the HTTP server (<http://127.0.0.1:8080>).

watch
> Runs css:watch, livereload, and http-server.
