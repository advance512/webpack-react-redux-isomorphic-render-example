This sample project is a proof-of-concept for isomorphic (universal) Webpack rendering using React.

Features

* React (+ hot reload for React components and Redux reducers in development mode)
* React-router
* Redux as Flux
* Isomorphic (universal) rendering
* Webpack
* Koa

Quick Start
===========

* `npm install`
* `npm run dev`
* wait for it to finish (it will say "Now go to http://127.0.0.1:3000" in the end)
* go to `http://localhost:3000`
* interact with the development version of the web application
* `Ctrl + C`
* `npm run production`
* wait a bit for Webpack to finish the build (green stats will appear in the terminal, plus some `node.js` server running commands)
* go to `http://localhost:3000`
* interact with the production version of the web application

Motivation
==========

In summer 2015 I wrote [`webpack-isomorphic-tools`](https://github.com/halt-hammerzeit/webpack-isomorphic-tools) to make isomorphic (universal) React rendering work on server-side when the project was built with Webpack.

The goal was met and many people started using it to implement isomorphic (universal) rendering in their apps.

Half a year passed and then I decided to give a try to the obscure enough [`target: 'node'`](https://github.com/webpack/react-starter) Webpack option which is the officially recommended way of setting up isomorphic (universal) rendering when building apps with Webpack. I used [sokra](https://github.com/sokra)'s [`react-starter`](https://github.com/webpack/react-starter) as a reference with a goal of making it much easier to use and much more developer-friendly.

Status
======

Seems to work. An `npm` module library will be released once this code is tested enough.

If you have any issues running this code you can report them the issue tracker.

To do
==========

 * Maybe fix [hot module reloading](https://webpack.github.io/docs/hot-module-replacement.html) for '../model' inside Redux store (hot reload Redux stores)

 * Move "webpack-react-isomorphic-render" to a separate npm package

 * Maybe fix the "Clean webpack did not delete path: ...\webpack-react-redux-isomorphic-render-example\build\assets" error

 * Remove obsolete commented code

 * Maybe make server side rendering Webpack code source maps work for exception stack traces. Currently Node.js [doesn't support source maps](https://github.com/nodejs/node-v0.x-archive/issues/3712).

 * Maybe try multiple entry points on client side (nah)