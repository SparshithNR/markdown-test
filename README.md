# DocTester

This library is used to test the code samples in the docments. Using this library you can always ensure that code samples in docments always work and avoids issues created for document update.

## Installation
```sh
npm install sparshithNR/doc-tester#master --save-dev
```
## Usage
### From commandline
```sh
node_modules/.bin/doc-tester
```
#options
1. -f (--file)
> File name/path which is to be tested. Defaulted to `README.md` in the root.
2. -d (--debug)
> Setting this to true will not remove the test file generated by parsing the documentation file. Defaulted to `false`.
3. --inspect (--inspect-brk)
> This will enable you to put debugging break points in test file. Defaulted to `false`.
4. -o (--output)
> Path/name where you want test file generated need to be placed once code is generated. Default path/name `test.js` and created in root directory.
### From code
```js
import { runTest } from 'doc-tester';
await runTest({
  codeArray: ['add(3,4) // equals: 7;'],
  importsArray: [`import { add } from './add'`]
} /* , options */);
```
### Options
1. testName
> Name for the test block. Defaulted to `Doc Test`.
2. debug
> Setting this to true will not remove the test file generated by parsing the documentation file. Defaulted to `false`.
3. inspect
> This will enable you to put debugging break points in test file. Defaulted to `false`.
4. testFile
> Path/name where you want test file generated need to be placed once code is generated. Default path/name `test.js` and created in root directory.