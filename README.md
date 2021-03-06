## Website & 0x Portal DApp

This repository contains our website and [0x Portal DApp][portal-url] (over-the-counter exchange), facilitating trustless over-the-counter trading of Ethereum-based tokens using 0x protocol.

[website-url]: https://0x.org/
[portal-url]: https://0x.org/portal

## Contributing

We strongly recommend that the community help us make improvements and determine the future direction of the protocol. To report bugs within this package, please create an issue in this repository.

Please read our [contribution guidelines](../../CONTRIBUTING.md) before getting started.
## Local Dev Environment
It allows us to set up a server  environment on our own machine ,instead of using the server environment provided by your hosting company.
## Components of Local Dev Environment
*Version control
*A local Web Server
*Package managers
*Task Runner
*Testing and Debug Environment
*Professional IDE
*Sniffer to sniff out

## How to Set up a Local dev Environment

Requires Node version 6.9.5 or higher

Add the following to your `/etc/hosts` file:

```
127.0.0.1 0xproject.localhost
local host:8000
```

You will also need to have the [aws CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html) installed locally and your credentials set up.

### Install dependencies:

```bash
yarn install
```

### Initial setup

To build this package and all other monorepo packages that it depends on, run the following from the monorepo root directory:

```bash
yarn build
```

### Run dev server

```bash
yarn dev
```

Visit [0xproject.localhost:3572](http://0xproject.localhost:3572) in your browser.

### Clean

```bash
yarn clean
```

### Lint

```bash
yarn lint
```

### Indexing docs

Before you can index the docs on Algolia, you need to set the admin API key environment variable:

```
# 0x Website frontend
export ALGOLIA_ADMIN_API_KEY={YOUR_ADMIN_API_KEY}
```

```bash
yarn index_docs
```

The above script will index all the docs found in the `/mdx` folder on [Algolia](https://www.algolia.com/). It's possible to pass in arguments that match the directory names to index only those document types, i.e. `yarn index_docs --indexes 'tools,core-concepts' --environment development` will index tools and core concepts for `development`.

Running the script updates some of the meta information about the files (relative paths to files and versions of the doc). For other types of information (i.e. title, subtitle, tags...) you will have to update it yourself.

### Resources

##### Toolkit

-   [Material Design Icon Font](http://zavoloklom.github.io/material-design-iconic-font/icons.html#directional)
-   [BassCSS toolkit](http://basscss.com/)
-   [Material-UI component library](http://www.material-ui.com/#/)

##### Recommended Atom packages:

-   [atom-typescript](https://atom.io/packages/atom-typescript)
-   [linter-tslint](https://atom.io/packages/linter-tslint)
