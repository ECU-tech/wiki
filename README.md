# Wiki

This is the source code for the ECU-tech Wiki - [wiki.ecu.tech](https://wiki.ecu.tech).

## Development

ECU-tech Wiki is built using [Docusaurus 2](https://docusaurus.io/).

### Installation

Required [Node.js](https://nodejs.dev/) is defined in [.nvmrc](/.nvmrc). If you use [nvm](https://github.com/nvm-sh/nvm), run `nvm use` to switch to the correct version.

To install dependencies, run:

```bash
npm install
```

### Local Development

```bash
npm start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

Docusaurus guides: [https://docusaurus.io/docs/category/guides](https://docusaurus.io/docs/category/guides)

#### Lint code

```bash
npm run lint

npm run lint:fix
```

### Build

```bash
npm run build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Redirection

Some addresses have client-side redirection set up here: [docusaurus.config.js](/docusaurus.config.js) (section `redirects: [...]`).

Those addresses come from the INI files (TS & HT). This gives more flexibility when wiki pages are moved or renamed.

Example:

```bash
https://wiki.ecu.tech/r/fuel -> https://wiki.ecu.tech/category/fuel/
```

### Generate PDF

Required [Prince XML](https://www.princexml.com/).

Build and serve docs locally before generating PDF:

```bash
npm run build
npm run serve
```

In another terminal, run this to generate PDF:

```bash
npm run pdf
```
