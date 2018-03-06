# Ebookcoin

亿书：加密货币驱动的电子书写作和版权保护应用。源码解析与开发指南：[《Nodejs开发加密货币》][]，官方开发交流群：185046161

Ebookcoin is a decentralized application for eBook-writing and copyright-protection powered by the next-generation Crypto Currency. For more information please refer to our website: http://ebookchain.org/.

## Installation

**NOTE:** The following is applicable to: **Ubuntu 14.04 (LTS) - x86_64**.

Install essentials:

```
sudo apt-get update
sudo apt-get install curl build-essential python
```

Install SQLite3 (version 3.8.2):

```
apt-get install -y sqlite3
```

Install Node.js (version 0.12.x) + npm:

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh | bash
nvm install 0.12.14
```

Install grunt-cli (globally):

```
npm install grunt-cli -g
```

Install bower (globally):

```
npm install bower -g
```

Install node modules:

```
npm install
```

Load git submodules ([client](https://github.com/Ebookcoin/client) and [ebookcoin-js](https://github.com/Ebookcoin/ebookcoin-js))，[Error: Permission denied (publickey)?](https://help.github.com/articles/error-permission-denied-publickey/):

```
git submodule init
git submodule update
```

Build the user-interface:

```
cd public
npm install
bower install
grunt release
```

## Launch

To launch Ebookcoin:

```
node app.js
```

**NOTE:** The **port**, **address** and **config-path** can be overridden by providing the relevant command switch:

```
node app.js -p [port] -a [address] -c [config-path]
```

## Tests

Before running any tests, please ensure Ebookcoin is configured to run on a local testnet (this is the default), and not the mainnet.

Install mocha (globally):

```
npm install mocha -g
```

Run the test suite:

```
npm test
```

Run individual tests:

```
mocha test/lib/accounts.js
mocha test/lib/transactions.js
```

## License

The MIT License (MIT)  

Copyright (c) 2016 Ebookcoin  
Copyright (c) 2014-2015 Crypti  


[《Nodejs开发加密货币》]: http://bitcoin-on-nodejs.ebookchain.org
