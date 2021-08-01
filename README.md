# esbuild-plugin-gzipper
An esbuild plugin to gzip output files

## Installation

yarn:
```sh
yarn add esbuild-plugin-gzipper --dev
````

NPM:
```sh
npm install --save-dev esbuild-plugin-gzipper
```

## Usage

```js
import { build } from 'esbuild';
import { gzipper } from 'esbuild-plugin-gzipper';

build({
	entryPoints: ['input.js'],
	outfile: 'output.js',
	bundle: true,
	plugins: [gzipper({
    compress: true,
	})],
}).catch(e => {
    console.error(e);
    process.exit(1);
});
```
## Configuration
The plugin responds to the following configuration options:
```javascript
gzipper({
    compress: boolean,      // should the finial output be compressed (gzip)
                            // DEFAULT: false 
});
```
