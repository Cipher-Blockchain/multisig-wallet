# Ethereum Multisignature Wallet

## Uses Node Version 6.17.1...for the initial build and 14 for running stuff...

```
nvm install 6.17.1
nvm use 6.17.1
```

## Features

- Can hold Ether and all kind of tokens with multisig support
- Easy to use offline signing (cold wallet) support
- Integration with web3 wallets (Metamask, Mist, Parity, etc)
- Transaction data and log decoding, makes transactions more readable
- Interacting with any contracts with UI support
- Hardware wallet support (Ledger Wallet)
- Optional email notifications when an event is triggered or you are required to sign a transaction

## Being used by

- [Aragon](https://aragon.one/)
- [Bancor](https://www.bancor.network/)
- Brace
- [District0x](https://district0x.io/)
- [Golem](https://golem.network/)
- [MysteriumNetwork](https://mysterium.network/)
- [Weifund](http://weifund.io/)
- StabL

## Install

```
# For Ubuntu/Debian you need to install libusb development headers
sudo apt install -y libusb-1.0-0-dev

git clone https://github.com/gnosis/MultiSigWallet.git
cd MultiSigWallet

# Latest NodeJS (v12.13.0) does NOT appear to work correctly.
# You should use NVM and install Node v6.17.1 for best results: https://github.com/nvm-sh/nvm
# Tested by @Privex on 2019-Nov-06 with v6.17.1 with success
sudo nvm install v6.17.1

# node-gyp is required for 'npm install' to work correctly
sudo npm install node-gyp

npm install
```

## Test

### Run contract tests:

```
npm test
```

### Run interface tests:

```
npm run test-dapp
```

## Deploy Contracts

### Deploy multisig wallet:

```
truffle migrate <account1,account2,...,accountN> <requiredConfirmations>
```

### Deploy multisig wallet with daily limit:

```
truffle migrate <account1,account2,...,accountN> <requiredConfirmations> <dailyLimit>
```

## Deployed instances

## Helper
