# poc_typescript

To complie a single typescript file to a javascript file: greeter.ts --> greeter.js

``` powershell
tsc greeter.ts 
```

## esbuild

An extremely fast JavaScript bundler.  [Project Page](https://esbuild.github.io/)

To install esbuild, create the node_modules folder then use npm:

``` powershell
npm install esbuild

.\node_modules\.bin\esbuild --version

```

To minify:

``` powershell
.\node_modules\.bin\esbuild greeter.js --bundle --outfile=greeter.min.js
```

Add the following to the package.json

``` json
 "scripts": {
    "build": "esbuild greeter.ts --bundle --outfile=greeter.min.js"
  }
```

Then to build: 

``` powershell
npm run build
```