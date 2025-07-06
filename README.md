# LocalProxy Community Extensions Registry

This repository contains the registry of community extensions for LocalProxy.

## How it works

The `registry.json` file contains metadata about available extensions. LocalProxy clients can fetch this file to discover and install community extensions.

## Registry Format

```json
{
  "version": "1.0",
  "extensions": {
    "extension-id": {
      "name": "Extension Display Name",
      "version": "1.0.0",
      "url": "https://raw.githubusercontent.com/localproxy-community/extension-id/main/index.js"
    }
  }
}
```

## Adding Your Extension

To add your extension to the registry:

1. Create a repository under the `localproxy-community` organization
2. Add your extension code as `index.js` in the main branch
3. Submit a PR to this repository updating `registry.json`

## Extension Requirements

- Extensions must be written in JavaScript (not TypeScript)
- Extensions must export the required interface (metadata, urlPatterns, onRequest, onResponseStreamTransform)
- Extensions should be self-contained and not require external dependencies