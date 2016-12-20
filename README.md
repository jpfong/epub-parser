# simple-epub-parser

> An easy-to-use epub parser written in TypeScript. 

The package exports a simple parser function which input epub file and output as JavaScript object. The output object is consisted of `nav`, `flesh` and `meta`.

`flesh` is epub's content and it is in the format of markdown.

As it is written in TypeScript, types are already included in the package.

## Install

``` bash
npm install simple-epub-parser --save
```

## Usage

```js
import parser from 'simple-epub-parser'

console.log('epub content:', parser('/path/to/file.epub'))
console.log('epub content:', parser(binaryData, true))
```

### parser(target?: string | buffer, options?: object)

#### target

type: `string` or `buffer`

It can be the path to the file or file's binary string or buffer

#### options

type: `object`

##### type?: 'binaryString' | 'path' | 'buffer'

It forces the parser to treat supplied target as the defined type, if not defined the parser itself will decide how to treat the file (useful when you are not sure if the path is valid).
