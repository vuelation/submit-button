# Vuelation Submit Button

A Vue.js component for submitting a form with a confirmation dialog that will add the button name to the submitted params like in Rails.

## Installation

Install via [npm](https://www.npmjs.com):

```sh
$ npm install vuelation-submit-button --save
```

Add [webpack](http://webpack.github.io) config:

```js
{
  module: {
    loaders: [{
      test:    /\.vue$/,
      loaders: ['vue']
    }]
  }
}
```

## Usage

Register the Vue component:

```js
Vue.component('submit-button', require('vuelation-submit-button'));
```

Use the component:

```html
<submit-button name="save" value="Save as Draft"></submit-button>
```

Add a confirmation prompt:

```html
<submit-button name="save" value="Save as Draft" confirm="Are you sure?"></submit-button>
```
