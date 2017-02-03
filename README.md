# systemjs-less-plugin

Translates less on the browser, inlines CSS conversion during build. 

[![npm](https://img.shields.io/npm/dm/systemjs-less-plugin.svg?style=plastic)](https://www.npmjs.com/package/systemjs-less-plugin) [![Code Climate](https://codeclimate.com/github/HuasoFoundries/systemjs-less-plugin/badges/gpa.svg)](https://codeclimate.com/github/HuasoFoundries/systemjs-less-plugin) [![Travis CI](https://travis-ci.org/HuasoFoundries/systemjs-less-plugin.svg)](https://travis-ci.org/HuasoFoundries/systemjs-less-plugin)

This SystemJS plugin provides in-browser compilation of less stylesheets to regular CSS styles,
as well as precompilation at the build stage when bundling your project with JSPM.

It depends (of course) on [{Less}](http://lesscss.org/) but you don't need to worry about it. 
We have it bundled along this loader plugin. It also depends on [plugin-css](https://github.com/systemjs/plugin-css) and,
again, you don't need to worry about that, because it'll be installed along `system-less-plugin`.


### Installing

To use this plugin, install it with jspm like so:

```sh
jspm install less
```

Then, in your jspm.config file, add less as the loader for less files (duh!):

```js
SystemJS.config({
  paths: {...}
  map: {...}
  meta: {
    '*.less': { loader: 'less' }
  }
});
```


### Configuration and options

This plugin is built on top of the [CSS plugin base](http://github.com/systemjs/plugin-css) which provides most of its features.
As such, system-less-plugin supports the same [build options](https://github.com/systemjs/plugin-css#builder-support).

Among other features, this includes source maps and generation of separate CSS files.


#### In case npm is down...

It's very uncommon for NPM to be down, but if that's your case or
for any other reson you rather use github, then this is the way:

```sh
jspm install less=github:huasofoundries/systemjs-less-plugin
````



License
---

MIT


