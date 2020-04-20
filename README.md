<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@200;700&display=swap" rel="stylesheet">
<div align="center" style="font-family: 'Nunito', sans-serif;">
  <img width="120" height="120" src="https://webpack.js.org/assets/icon-square-big.svg">
  <h1 style="margin: 5px 0;">Webpack Template</h1>
  <p>
    Webpack is a module bundler. Its main purpose is to bundle JavaScript files for usage in a browser, yet it is also capable of transforming, bundling, or packaging just about any resource or asset.
  </p>
</div>


### Info

###### Download repository:
`git clone https://github.com/YuriShvetsov/webpack-template folder`

###### Install dependencies:
`npm i`

###### Server with hot reload at http://localhost:9000/
`npm run dev`

###### Output will be at dist
`npm run build`


### Project Structure

* `src/index.html` - main app HTML
* `src/assets/scss` - put custom app SCSS styles here. Don't forget to import them in `index.js`
* `src/assets/css` - the same as above but CSS here. Don't forget to import them in `index.js`
* `src/assets/images` - put images here. Don't forget to use correct path: `assets/images/some.jpg`
* `src/js` - put custom app scripts here
* `src/index.js` - main app file where you include/import all required libs and init app

<div style="text-align: center; text-transform: uppercase;">
  <h3>Settings</h3>
</div>

### Default paths

Easy way to move all files

``` js

const PATHS = {
  // Path to main app dir
  src: path.join(__dirname, '../src'),
  // Path to Output dir
  dist: path.join(__dirname, '../dist'),
}
```

### Import another libs

1. Install libs
2. Import libs in `./index.js`

``` js
// React example
import React from 'react'
// Bootstrap example
import Bootstrap from 'bootstrap/dist/js/bootstrap.min.js'
import 'bootstrap/dist/js/bootstrap.min.js'
```

### Import only SASS or CSS libs

1. Install libs
2. Go to `/assets/scss/utils/libs.scss`
3. Import libs in node modules

``` scss
// CSS librarys example:
@import '../../node_modules/flickity/dist/flickity.css';
// Sass librarys example:
@import '../../node_modules/spinners/stylesheets/spinners';
```

### Import JS files

1. Create another js module in `./js/` folder
2. Import modules in `./js/index.js` file

``` js
// another JS file for example
import './common.js'
```

### Add fonts
Add @font-face in `/assets/scss/utils/fonts.scss`:

``` scss
// Example with Lora
@font-face {
    font-family: 'Lora';
    src: url('../fonts/Lora/Lora-Regular.eot');
    src: url('../fonts/Lora/Lora-Regular.eot?#iefix') format('embedded-opentype'),
        url('../fonts/Lora/Lora-Regular.ttf') format('truetype'),
        url('../fonts/Lora/Lora-Regular.woff2') format('woff2'),
        url('../fonts/Lora/Lora-Regular.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}
```

### Variables in SCSS

Add vars in `/assets/scss/utils/vars.scss`:

``` scss
// Fonts
$main-font: 'Lora', Arial, sans-serif;
```