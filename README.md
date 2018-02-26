# w3c-keys
[![Build Status](https://travis-ci.org/ashubham/w3c-keys.svg?branch=master)](https://travis-ci.org/ashubham/w3c-keys)
[![npm version](https://badge.fury.io/js/w3c-keys.svg)](https://badge.fury.io/js/w3c-keys)
[![npm](https://img.shields.io/npm/dm/w3c-keys.svg)](https://www.npmjs.com/package/w3c-keys)

<img src="https://github.com/ashubham/w3c-keys/raw/master/assets/keys.jpg" align="right" alt="w3c-keys" />

keyboardEvent.key compatible key codes with Typescript Definitions.

Read https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/key

Compatible with IE/Edge/Safari Key idiosyncrasies.

## Usage

```typescript
import { Key } from 'w3c-keys';

// To dispatch Events.
let evt = new KeyboardEvent('keydown', {
    key: Key.Space
});
document.body.dispatchEvent(evt);

// To check event keys.
document.body.on('keydown', (e) => {
    if(e.key === Key.Backspace) {
        // Do some shiz...
    }
});
```

## Why not use evt.which keyCodes ?

- `evt.which` keycodes are a deprecated standard.
- Ability to create synthetic key events which is not possible with `evt.which`.
