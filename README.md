# web-player

This project is generated with [yo angular generator](https://github.com/yeoman/generator-angular)
version 0.15.1.

## Initial start up

We are using node.js and npm to develop our project.
You should install node.js 4.x  version from [official site](https://nodejs.org/en/download/).

Run `n  t` to install all necessary npm and bower dependencies.

Run `npm install -g jasmine-node` to install jasmine-node globally. It will allow you to run "[frisby](http://frisbyjs.com/)" tests for REST API.

## Build & development

Run `grunt serve` for dev preview which is pointing to INT environment.

Run `grunt serve:dist` for preview packaged version.

Run `grunt serve:prod` for dev preview which is pointing to PROD environment.

Run `grunt build` to build app for PROD environment.

Run `grunt build:dev` to build app for DEV environment.

## Marketing template

after changes in marketing files (/marketing) do `grunt build`

then run file dist/static/index.html (do not forget to change urls for js and css files to local one)

## Testing

Running `grunt test` will run the unit tests with karma.

Running `jasmine-node test/api` will run unit test for REST API.


## Add new Controller, Service, Directive

Use yeoman for adding new angular entities. See examples below:

`yo angular:controller user`

More examples at [Yeoman Angular Generator](https://github.com/yeoman/generator-angular#readme) page.

**Attention!** We are using ui-router instead of builtin ng-router that is why you should
add routes manually.

## Project Notes

You shouldn't add `/scripts/config.js` to VCS. It's generated dynamically and contains environment (production/development) configuration.

We are using WebStorm as a primary IDE for developing and [jscs](https://www.npmjs.com/package/jscs) && [jshint](https://www.npmjs.com/package/grunt-contrib-jshint) npm modules for consistent code style.

You should use it as a pre-commit hook. To configure pre-commit GIT hook go to `.git/hooks` directory at project root.

Create new file with name `pre-commit`. Add next content:

`#!/bin/sh`
`grunt checkCodeAndStyle`

Now any time you will try to commit jscs and jshint will check your code for consistency. To get more detailed and convenient info
about issue go to cmd and try `grunt checkCodeAndStyle` or `grunt jscs`, `grunt jshint` for separate check.
#   W e b I R  
 