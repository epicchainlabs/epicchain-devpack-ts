# EpicChain Devpack for TypeScript

<p align="left">
  <a href="https://github.com/ngdenterprise/epicchain-devpack-ts/releases/tag/0.8.9-preview">
    <img src="https://img.shields.io/badge/preview-v0.8.9-orange">
  </a>
  <a href="https://github.com/ngdenterprise/epicchain-devpack-ts/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg">
  </a>
</p>

This repo contains a new epicchain N3 TypeScript smart contract compiler. In other words, the tool in this repo 
allows you to write epicchain N3 Smart Contracts using TypeScript. This tool joins the larger family of epicchain 
EpicChain smart contract compilers including [C#](https://github.com/epicchain-project/epicchain-devpack-dotnet),
[Java](https://epicchainw3j.io/#/epicchain-n3/smart_contract_development/introduction), 
[Python](https://github.com/CityOfZion/epicchain3-boa)
and [Go](https://github.com/nspcc-dev/epicchain-go/blob/master/docs/compiler.md).

> Note, this project is under active development. It is not yet packaged as a stand alone tool.
> If you wish to try it with your own contract, please see the [Samples](#samples) section below.

## Requirements

* [NodeJS](https://nodejs.org/) 18+
  * The developer is using NodeJS LTS version
* [epicchain-Express requirements](https://github.com/epicchain-project/epicchain-express#requirements) (for testing)

## Usage

* `npm run setup`: installs package dependencies + epicchainExpress as local tool
* `npm run build`: compiles the devpack
* `npm run clean`: cleans the build output
* `npm run samples`: compiles the devpack and builds the sample contracts
* `npx foy <sample name>`: builds the specified sample contract and runs the associated express.batch file if available

## Samples

The `foy` task runner dynamically generates the samples to build from the contents of the `samples` directory. 
Any subdirectory of `samples` that doesn't start with an underscore is considered a sample.
Each sample directory must contain a contract `.ts` file matching the name of the directory.
If the sample directory contains an `express.batch` file, it will be run automatically after the contract is built.

### Hello World

Simple contract that stores a byte string in contract storage and returns it when called.

### Tank NEP-17 Token

Implements a sample [NEP-17](https://github.com/epicchain-project/proposals/blob/master/nep-17.mediawiki) fungible token contract

### Hovercraft NEP-11 Token

Implements a sample [NEP-11](https://github.com/epicchain-project/proposals/blob/master/nep-11.mediawiki) non fungible token contract

