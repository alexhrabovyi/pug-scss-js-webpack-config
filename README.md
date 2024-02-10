# PUG + SCSS + JS webpack config 
This is a config for PUG, SCSS that uses Webpack, ESLint, Stylelint, Babel and other tools.

## Features
### Build
- config automatically creates entry properties for pages according to this path - src/pages/page_name/page_name.js, so you don't have to 
write entries by yourself for every page that you have
### HTML/PUG
- compilation PUG to HTML;
- automatically creates HTML file with content from necessary template;
- automatically connects JS and CSS files;

Production:
- minimizing;

### SCSS
- compilation SCSS to CSS;
- Stylelint with SCSS style rules;

Development:
- injects in HTML as an inline string to better rebuild performance;
- creates source maps;

Production:
- creates separate bundle file for every page;
- minimizing;
- file names with hash;
- adds vendor prefix by Autoprefixer;
- source maps aren't created;
- automatically executes `stylelint --fix`. If any unfixed errors left, build doesn't get created;

### JS
- creates separate bundle file for every page;
- ESLint;

Development:
- creates source maps;

Production:
- minimizing;
- mangling
- treeshacking
- transpiles and adds polyfills
- automatically executes `eslint --fix`. If any unfixed errors left, build doesn't get created;

### Images
- automatically generates in dist folder;

Production:
- file names with hash;
- minimizing;

### Fonts
- automatically generates in bundle folder;
- file names with contenthash;

### Favicons 
- automatically generates in dist folder;
- automatically connects to HTML file;

Development:
- generates one icon for better performance

Production:
- generates all kinds of favicons for better compatibility;

### Other
- DevServer by browser-sync;
- automatically cleans bundle folder before rebuilds

## Commands
- `eslint` - check files with eslint;
- `esling --fix` - check and fix files with eslint;
- `stylelint` - check files with stylelint;
- `stylelint --fix` - check and fix files with stylelint;
- `browser`- start local server and watch for files;
- `build:dev` - execute development build;
- `build:prod` - execute production build;
- `build:watch` - execute development build and watch for files;
- `serve` - execute development build, watch for files and start local server

## File Structure
dist <br />
src <br />
|_assets <br />
&nbsp;&nbsp;|_favicons <br />
&nbsp;&nbsp;|_fonts <br />
|_blocks <br />
|_elements <br />
|_js-libs <br />
|_pages <br />
|_scss <br />

## File Structure Example 
dist <br />
src <br />
|_assets <br />
&nbsp;&nbsp;|_favicons <br />
&nbsp;&nbsp;&nbsp;&nbsp;|_favicon.png <br />
&nbsp;&nbsp;|_fonts <br />
&nbsp;&nbsp;&nbsp;&nbsp;|_Roboto <br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|_Roboto-Bold.ttf <br />
|_blocks <br />
&nbsp;&nbsp;|_footer <br />
&nbsp;&nbsp;&nbsp;&nbsp;|_footer.js <br />
&nbsp;&nbsp;&nbsp;&nbsp;|_footer.pug <br />
&nbsp;&nbsp;&nbsp;&nbsp;|_footer.scss <br />
&nbsp;&nbsp;|_header <br />
&nbsp;&nbsp;&nbsp;&nbsp;|_header.js <br />
&nbsp;&nbsp;&nbsp;&nbsp;|_header.pug <br />
&nbsp;&nbsp;&nbsp;&nbsp;|_header.scss <br />
|_elements <br />
&nbsp;&nbsp;&nbsp;&nbsp;|_button.scss <br />
|_js-libs <br /> 
&nbsp;&nbsp;&nbsp;&nbsp;|_telMask.js <br /> 
|_pages <br /> 
&nbsp;&nbsp;&nbsp;&nbsp;|_main <br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|_main.js <br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|_main.pug <br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|_main.scss <br /> 
|_scss <br /> 
&nbsp;&nbsp;|_fonts.scss <br />
&nbsp;&nbsp;|_mixins.scss <br />
&nbsp;&nbsp;|_normalize.scss <br />