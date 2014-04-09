# grunt-ember-i18n-precompile [![Build Status](https://travis-ci.org/karl-sjogren/grunt-ember-i18n-precompile.png?branch=master)](https://travis-ci.org/karl-sjogren/grunt-ember-i18n-precompile)

This is a helper task for [Ember.I18n](https://github.com/jamesarosen/ember-i18n) that let you easily split your language files into several per language that are then combined using grunt. 

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-ember-i18n-precompile --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-ember-i18n-precompile');
```

## The "ember_i18n_precompile" task

### Overview
In your project's Gruntfile, add a section named `ember_i18n_precompile` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  ember_i18n_precompile: {
    english: {
      src: ['app/locales/en/base.js', 'app/locales/en/dashboard.js'],
      dest: 'dest/en.js'
    },
    german: {
      src: ['app/locales/de/base.js', 'app/locales/de/dashboard.js'],
      dest: 'dest/de.js'
    },
  },
})
```

### Usage Examples

#### Default Options

```js
grunt.initConfig({
  ember_i18n_precompile: {
    files: {
      'dest/en.js': 'app/languages/en.js'
    },
  },
})
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).