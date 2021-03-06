# The MetaMask Stack

[![Greenkeeper badge](https://badges.greenkeeper.io/MetaMask/Eth-Token-Sender.svg)](https://greenkeeper.io/)

[Live Example](https://flyswatter.github.io/MetaMaskStack/)

A composable boilerplate for writing Ethereum dapps in a similar environment to what the MetaMask developers use themselves to develop MetaMask.

Forked from my older [react-hyperscript-beefy-boilerplate](https://github.com/flyswatter/react-hyperscript-beefy-es6-boilerplate), which is not Ethereum specific.

## Purpose

I've been contributing to MetaMask for a while, and I wanted to make a web dapp with ethjs that used a similar build system.

My friend Jared said it was a nice little framework, and I should do a better job of sharing it.

It also crossed my mind that this framework could be good practice for onboarding MetaMask contributors.

## Features

- Adds an instantiated [ethjs](https://github.com/ethjs/ethjs) object onto the state object for easy ethereum interaction.
- Uses [react-hyperscript](https://www.npmjs.com/package/react-hyperscript) with [Babel](https://www.npmjs.com/package/Babel) for an Elm-like Javascript ES6 experience.
- The sample project detects presence of the web3 API, and suggests downloading MetaMask in its absence.
- Features a simple tip button transaction, to show how easy it is to send a transaction and indicate loading state and errors.

## Usage

### Installation

Have node.js installed, then in the project folder:

```
npm install
```

### Development

To run with live-reloading via beefy:

`npm start`

To build:

`npm run build`

This will generate a `bundle.js` file that is pointed to by the `index.html`.

## Project Structure

```
./index.html                    <- The entry point for the app
./index.js                      <- The JS init entry point for the app, unbuilt.
./app                           <- The usually edited react views
├── root.js                     <- The home page, which could host routing, and has full state.
└── template.js                 <- Copy this to create views with full state access.
├── components                  <- The components that rely on local state
│   ├── download-metamask.js    <- A sample local React component, with customized style params!
│   └── template.js             <- Copy this to create your own components
./lib
├── reducers
│   └── index.js                <- The root React Redux reducer file.
└── store.js                    <- The redux store, instantiated with thunk and logging.
./bundle.js                     <- The built JS bundle, generated by `npm run build`.
```

## To Dos:

- [ ] Add nice style sheet management, like SASS.
- [ ] Add unit test suite
- [ ] Add browser test suite (testem?)

