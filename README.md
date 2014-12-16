# Microsite template

Supported browsers: Apple Safari 5+, Google Chrome 22+, Microsoft Internet Explorer 8+, Mozilla Firefox 16+, Opera Browser 12+ (older versions and other browsers may work, but these are the ones we verify). Development environment requires [Sass](http://sass-lang.com) and [Compass](http://compass-style.org), plus the Compass extensions [Breakpoint](https://github.com/Team-Sass/breakpoint) and [Singularity](http://singularity.gs).

## Requirements

Building this project requires:

* [Node.js](http://nodejs.org/) >=0.8.0
* [Ruby](http://www.ruby-lang.org/en/)
* [Bundler](http://bundler.io/)
* [Grunt](http://gruntjs.com/) ~0.4.0
* [Bower](http://bower.io/) >=0.10.0

## Setup

### Installing required tools

The project uses [Grunt](http://gruntjs.com/) to run tasks and [Sass](http://sass-lang.com/) for CSS pre-processing. First make sure you have base dependencies installed: [Ruby](http://www.ruby-lang.org/en/), [Node.js](http://nodejs.org/), [Bundler](http://bundler.io/), [Grunt](http://gruntjs.com/) and [Bower](http://bower.io/). You can install Node and Ruby using their installers, Bundler with gem and the rest with npm:

    $ gem install bundler
    $ npm install -g grunt-cli
    $ npm install -g bower

Consult the tools' documentation for more instructions.

### Installing dependencies

After you have the base dependencies taken care of, you can install the project's dependencies. Navigate to the project's directory, and run the dependency managers:

    $ cd txpmag-website
    $ npm install
    $ bundle install
    $ bower install

*npm* installs Node modules for Grunt, *bundle* takes care of Ruby gems, and *bower* manages client-side scripts.

## Building

This repository hosts sources and needs to be built before it can be used. After you have installed all dependencies, you will be able to run tasks using Grunt, including building:

    $ grunt [task]

Where the `[task]` is either `test`, `build` or `watch`. Watch will launch a task that watches for file changes. The project is automatically built if a source file is modified. The build task builds the project.

Source files are within the `src` directory, built files are within the `public` directory (this would also be the root directory of a site build).

## Global namespacing

The HTML file references two CSS stylesheets: `global.css` and `local.css` (and their corresponding Sass files `global.scss` and `local.scss`).

The `global.css` file contains rules that will be common across all microsites. Any classnames used with this stylesheet will be prefixed with `.global-`. *The global styleheet should not be changed in any way.*

All CSS rules specific to a microsite design should be added to the `local` file, and should never prefixed with `.global-`.
