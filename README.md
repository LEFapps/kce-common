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
@import "../kce-common/css/_settings", "<your custom settings>", "../kce-common/css/_common";
```

Note that the inclusion of `_common.scss` automatically includes bootstrap as well. So the complete load order is this:

* Common KCE scss settings (variables)
* Custom overrides of scss variables
* Shared KCE components, configured by variables
* Bootstrap, configured by variables

## Sections

Due to 11ty / liquid restrictions, you can not include files from outside the _includes folder in your templates. Solve this by symlining the section folder in this repo in your _includes folder:

```shell
$ cd _includes
$ ln -s ../kce-common/sections
```
