# npmdoc-milligram

#### api documentation for  [milligram (v1.3.0)](https://milligram.github.io)  [![npm package](https://img.shields.io/npm/v/npmdoc-milligram.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-milligram) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-milligram.svg)](https://travis-ci.org/npmdoc/node-npmdoc-milligram)

#### A minimalist CSS framework.

[![NPM](https://nodei.co/npm/milligram.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/milligram)

- [https://npmdoc.github.io/node-npmdoc-milligram/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-milligram/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-milligram/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-milligram/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-milligram/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-milligram/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "milligram",
    "version": "1.3.0",
    "description": "A minimalist CSS framework.",
    "homepage": "https://milligram.github.io",
    "repository": "milligram/milligram",
    "license": "MIT",
    "author": "CJ Patoilo <cjpatoilo@gmail.com>",
    "main": "dist/milligram.css",
    "keywords": [
        "bootstrap",
        "css",
        "css3",
        "flexbox",
        "front-end",
        "framework",
        "html",
        "html5",
        "kickstarter",
        "less",
        "responsive",
        "mobile",
        "mobile-first",
        "postcss",
        "responsive",
        "sass",
        "scss",
        "stylus"
    ],
    "ignore": [
        ".appveyor.yml",
        ".editorconfig",
        ".eslintrc",
        ".github",
        ".gitignore",
        ".npmignore",
        ".sasslintrc",
        ".travis.yml",
        "backstop.conf.js",
        "bower.json",
        "changelog.md",
        "composer.json",
        "package.js",
        "package.json",
        "src",
        "test"
    ],
    "dependencies": {
        "normalize.css": "~5.0.0"
    },
    "devDependencies": {
        "autoprefixer": "^6.5.4",
        "ava": "^0.17.0",
        "backstopjs": "^2.3.5",
        "banner-cli": "^0.9.2",
        "browser-sync": "^2.18.5",
        "editorconfig-tools": "^0.1.1",
        "eslint": "^3.14.0",
        "eslint-config-styled": "^0.0.0",
        "husky": "^0.11.9",
        "node-sass": "^3.13.1",
        "npm-run-all": "^2.3.0",
        "nyc": "^10.0.0",
        "onchange": "^2.5.0",
        "postcss-cli": "^2.6.0",
        "rimraf": "^2.5.4",
        "sass-lint": "^1.10.2"
    },
    "engines": {
        "node": ">=4"
    },
    "scripts": {
        "start": "run-p build watch serve",
        "build": "run-s clean sass autoprefixer banner",
        "clean": "rimraf dist",
        "sass": "node-sass --output-style expanded src/milligram.sass dist/milligram.css && node-sass --output-style compressed src/milligram.sass dist/milligram.min.css",
        "autoprefixer": "postcss -u autoprefixer --no-map.inline --autoprefixer.browsers \"last 1 versions\" -r dist/*.css",
        "banner": "banner-cli dist/*.css",
        "watch": "onchange src -- run-p build",
        "serve": "browser-sync start --no-notify -s test --ss dist -f dist",
        "backstop": "run-s build && run-p serve compare",
        "reference": "backstop reference --configPath=backstop.conf.js",
        "compare": "backstop test --configPath=backstop.conf.js",
        "lint": "sass-lint -c .sasslintrc src --verbose --no-exit && eslint test -c styled && editorconfig-tools check .",
        "ava": "nyc ava",
        "test": "run-s build lint ava",
        "precommit": "run-p test"
    },
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
