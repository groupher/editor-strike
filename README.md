![](https://badgen.net/badge/Editor.js/v2.0/blue)

# Strike Tool

Strike Tool for highlighting text-fragments for the [Editor.js](https://editorjs.io).

![](assets/example.gif)

## Installation

### Install via NPM

Get the package

```shell
npm i --save-dev @editorjs/strike
```

Include module at your application

```javascript
const Strike = require("@editorjs/strike");
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

### Load from CDN

You can load specific version of package from [jsDelivr CDN](https://www.jsdelivr.com/package/npm/@editorjs/strike).

`https://cdn.jsdelivr.net/npm/@editorjs/strike@1.0.1`

Require this script on a page with Editor.js.

```html
<script src="..."></script>
```

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
var editor = EditorJS({
  ...

  tools: {
    ...
    Strike: {
      class: Strike,
      shortcut: 'CMD+SHIFT+M',
    }
  },

  ...
});
```

## Config Params

This Tool has no config params

## Output data

Marked text will be wrapped with a `mark` tag with an `cdx-strike` class.

```json
{
  "type": "text",
  "data": {
    "text": "Create a directory for your module, enter it and run <mark class=\"cdx-strike\">npm init</mark> command."
  }
}
```
