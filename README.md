cljs-nodejs-example
===================

An example of using ClojureScript to make a node.js app.

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

Requirements
============

* lein
* node.js

Steps
=====

Run the following from the base project directory:

    npm install
    lein cljsbuild once

This will create the target/js/myexample.js file. This is what you can run with node.js:

    node target/js/myexample.js

And there you go, a "Hello World!" that's over 12,000 lines of JavaScript!

Deploy
=====

Create a Heroku app

    heroku create
    heroku buildpacks:add heroku/nodejs
    heroku buildpacks:add heroku/clojure
    git push heroku master
