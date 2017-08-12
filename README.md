# w3c-keys

keyboardEvent.key compatible key codes with Typescript Definitions.

Read https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/key

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
