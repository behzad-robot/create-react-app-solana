# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

These Repo has Solana Labs Packages installed from this link:
https://github.com/solana-labs/wallet-adapter

So it has following solana web3 packages installed:

    "@solana/wallet-adapter-base": "^0.9.22",
    "@solana/wallet-adapter-react": "^0.15.30",
    "@solana/wallet-adapter-react-ui": "^0.9.29",
    "@solana/wallet-adapter-wallets": "^0.19.15",
    "@solana/web3.js": "^1.73.3",

# 😊 Do this without cloning this repo? 
The proccess is atually quite simple if you want to do it with your own create-react-app project:

    npm run eject

Then add these items to resolve section of your webpack.config.js:

    resolve:{
        // This allows you to set a fallback for where webpack should look for modules.
        fallback: {
            assert: require.resolve('assert'),
            buffer: require.resolve('buffer'),
            crypto: require.resolve('crypto-browserify'),
            stream: require.resolve('stream-browserify'),
        },
        //..... blah blah other config things
    },
    ignoreWarnings: [/Failed to parse source map/],
