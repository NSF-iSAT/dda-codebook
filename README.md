

# DRAFT: DDA Codebook Website

A prototype of a Website containing the DDA codebook with two goals in mind:

1. Making the DDA codebook semantic-versionable and parseable, for building prompts for DDA Parsing.
2. Making some of the conventions and decisions we note down from discussions an available resource for DDA Annotators after a corpus release.

This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator.

### Installation

```
$ yarn
```

### Local Development

```
$ yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

#### Note: Search Plugin Disabled in Local Development

The plugin `docusaurus-lunr-search` is used to enable a search bar/index over the built site. This has been disabled in development as to avoid repeatedly building and loading the search index. To test something in search, use `yarn build` followed by `yarn serve` to simulate a 'production' build locally.

### Build

```
$ yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

#### Serving

```
$ yarn serve
```
Serves the static site contained in the `build/` directory (from `yarn build`)

### Deployment

Using SSH:

```
$ USE_SSH=true yarn deploy
```

Not using SSH:

```
$ GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.
