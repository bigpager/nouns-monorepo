# CHANGES FOR MEKATOADZ DEVELOPMENT

## Running the site

> After cloning the repo to your local computer, do these steps:

1. `yarn` (this installs all dependencies)
1. `yarn build` (compiles code)
1. `yarn start` (encodes `png` --> `svg` and starts local web server)

> Now you should have the random generator running at http://localhost:3000/playground

---

## Updating the images

> MekaToadz source images are stored in:

```
    ./packages/nouns-assets/images
      /0-backgrounds
      /1-bodies
      /2-accessories
      /3-heads
      /4-glasses
            
```

> These directories contain a small subset of the Nouns images (to be replaced with MekaToadz images). 
> For reference, I copied the full collection of Nouns images to:

```
    ./packages/nouns-assets/images
      /sample-0-backgrounds
      /sample-1-bodies
      /sample-2-accessories
      /sample-3-heads
      /sample-4-glasses
            
```

## Restarting the site

1. Shut down the currently-running process (`Ctrl+C` in Windows)
1. Execute `yarn start` again (must be in the repo's root directory).

> This will re-encode any PNG images as SVGs and restart the local web server.

---

# nouns-monorepo

Nouns DAO is a generative avatar art collective run by a group of crypto misfits.

## Contributing

If you're interested in contributing to Nouns DAO repos we're excited to have you. Please discuss any changes in `#developers` in [discord.gg/nouns](https://discord.gg/nouns) prior to contributing to reduce duplication of effort and in case there is any prior art that may be useful to you.

## Packages

### nouns-api

The [nouns api](packages/nouns-api) is an HTTP webserver that hosts token metadata. This is currently unused because on-chain, data URIs are enabled.

### nouns-assets

The [nouns assets](packages/nouns-assets) package holds the Noun PNG and run-length encoded image data.

### nouns-bots

The [nouns bots](packages/nouns-bots) package contains a bot that monitors for changes in Noun auction state and notifies everyone via Twitter and Discord.

### nouns-contracts

The [nouns contracts](packages/nouns-contracts) is the suite of Solidity contracts powering Nouns DAO.

### nouns-sdk

The [nouns sdk](packages/nouns-sdk) exposes the Nouns contract addresses, ABIs, and instances as well as image encoding and SVG building utilities.

### nouns-subgraph

In order to make retrieving more complex data from the auction history, [nouns subgraph](packages/nouns-subgraph) contains subgraph manifests that are deployed onto [The Graph](https://thegraph.com).

### nouns-webapp

The [nouns webapp](packages/nouns-webapp) is the frontend for interacting with Noun auctions as hosted at [nouns.wtf](https://nouns.wtf).

## Quickstart

### Install dependencies

```sh
yarn
```

### Build all packages

```sh
yarn build
```

### Run Linter

```sh
yarn lint
```

### Run Prettier

```sh
yarn format
```
