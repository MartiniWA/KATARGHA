# KATARGHA
Katargha is an sub-module bundler for the CRA based projects, works without ejecting from CRA


# Yarn & NPM

```
yarn add katargha -D
```

```
npm install katargha --save-dev
```


# Basic configuration and usage

.katargha.json
```json
{
  "dir": {
    "src": "./sw-modules",
    "dist": "./build"
  },
  "importScript": true,
  "override": "./build/service-worker.js",
  "ignore": [
    "i-don't-need-this-service.js",
  ]
}
```

package.json
```
- "build": "react-scripts build"
+ "build": "react-scripts build && katargha -l"
```

## File Structure for Create React App
```
root/
  build/
    service-worker.js
  src/
    App.js
    ...
  .katargha.json
  /sw-modules
    module-1.js
    module-2.js
  index.js
  ...
```

# Command Line Args
  katargha -flag
  - -l [shows list available modules in pre-defined modules directory]
  - -c /path/to/conf.json [overrides config default location]

### TODO for .katargha.json
 - [x] Override support
 - [x] Output support
 - [ ] API for node-side internal configuration



# Package name
Katargha is a Georgian word კატარღა [k’at’argha] and means a small boat with an engine.
