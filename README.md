# Webpack backend basic configuration

[![Build Status](https://travis-ci.com/daniel-234/webpack-backend-basic-configuration.svg?branch=master)](https://travis-ci.com/daniel-234/webpack-backend-basic-configuration)

A minimal working configuration for backend projects in JavaScript bundled with Webpack.
This app skeleton configuration has been ejected from my other project [User authentication API](https://github.com/daniel-234/user-authentication-api) as a minimal working configuration for future backend projects and for reference. 

## Getting Started

TODO

## Built With

- [Express.js](https://expressjs.com/) - A minimalist web framework for Node.js
- [Jest](https://jestjs.io/en/) - A JavaScript testing library
- [Webpack](https://webpack.js.org/) - A static module bundler

## Author

- **Daniele Erbì** - [daniel-234](https://github.com/daniel-234)

## Notes

### Backend Apps with Webpack
Webpack, even in this basic configuration, showed this warning message when run.
```
WARNING in ./node_modules/express/lib/view.js 81:13-25
Critical dependency: the request of a dependency is an expression
@ ./node_modules/express/lib/application.js
@ ./node_modules/express/lib/express.js
@ ./node_modules/express/index.js
@ ./src/server.js
@ ./src/index.js
```
The solution suggested by [this](https://github.com/webpack/webpack/issues/196) issue was to use the package `webpack-node-externals` to avoid bundling `node-modules`. 
It's inspired by [this article](https://jlongster.com/Backend-Apps-with-Webpack--Part-I).

## License

This project is licensed under the MIT license.

## Acknowledgments

- [Twilio Blog - Working with Environment Variables in Node.js](https://www.twilio.com/blog/2017/08/working-with-environment-variables-in-node-js.html)
- [How to test Express.js with Jest and SuperTest](http://www.albertgao.xyz/2017/05/24/how-to-test-expressjs-with-jest-and-supertest/)
- [Backend apps with Webpack](https://jlongster.com/Backend-Apps-with-Webpack--Part-I)