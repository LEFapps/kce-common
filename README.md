# Common code for KCE apps

## Install

Add this repo as a submodule in your app:

```shell
$ git submodule add https://github.com/LEFapps/kce-common.git
```

Make sure you add this folder to your .eleventyignore file, otherwise it might be included in your _site build.

## CSS

You can now import files from kce-common in your `css/main.scss`:

```scss
@import
  '../kce-common/css/_settings',
  '../kce-common/css/components/_mixins',
  '../kce-common/css/imports/_base',
  '../kce-common/css/components/_splash',
  '../kce-common/css/components/_content',
  '../kce-common/css/components/_filter',
  '../kce-common/css/components/_nav',
  '../kce-common/css/components/_header',
  '../kce-common/css/components/_footer';

// Bootstrap
@import '../node_modules/bootstrap/scss/bootstrap';
```

## Sections

Due to 11ty / liquid restrictions, you can not include files from outside the _includes folder in your templates. Solve this by symlining the section folder in this repo in your _includes folder:

```shell
$ cd _includes
$ ln -s ../kce-common/sections
```
