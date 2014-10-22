loop-grid-mover
===

Move selected ranges of loops to new origin. [loop-grid](https://github.com/mmckegg/loop-grid) transform.

## API

```js
var Mover = require('loop-grid-mover')
```

### `var mover = Mover(transform)`

Pass `loopGrid.transform` to this constructor.

### `mover.start(inputGrid, selectedIndexes, done)`

Finds the top-left most coordinates in `selectedIndexes`, and uses this as the start origin. Any true values in `inputGrid` will call `transform` with a function that moves the values from selectedIndexes to the new origin. Multiple true values will cause the selectedIndexes to be duplicated.

### `mover.stop()`

Release any pending `transform` and stop watching `inputGrid`.