Snap.svg.FreeTransform
====================

  Free transform tool for [Snap.svg](http://snapsvg.io/) elements and sets with many options. Supports snap-to-grid dragging, scaling and rotating with a specified interval and range.

  Example can be found at http://svg.dabbles.info/Snap.svg.FreeTransform/ 

  Raphael version that this was based from can be found at https://github.com/AliasIO/Raphael.FreeTransform

  Forked from https://github.com/danny-toi/Snap.svg.FreeTransform (will try and feed back updates)


Options
-------

#### `animate: true | { delay: num, easing: string } | false`

Animate transformations. Works best in combination with `apply()` (see the functions section below).

Default: `{ delay: 700, easing: 'linear' }`


#### `attrs: { fill: hex, stroke: hex }`

Sets the attributes of the handles.

Default: `{ fill: '#fff', stroke: '#000' }`


#### `customCorners: { size: num, distance: num, corners: [ { action: string: image: string }, ... ] } | false

Specify custom images and events for corner handles.

The corners array should contain 4 objects, one for each corner starting top left going clockwise.

Valid actions: `drag`, `rotate`, `scale` or a custom string. Actions are emitted as events in the callback.

Default: `false`


#### `boundary: { x: int, y: int, width: int, height: int } | false`

Limits the drag area of the handles.

Default: dimensions of the paper


#### `distance: num`

Sets the distance of the handles from the center of the element (`num` times radius).

Default: `1.3`


#### `drag: true | [ 'center', 'self' ] | false`

Enables/disables dragging.

Default: `[ 'center', 'self' ]`


#### `draw: [ 'bbox', 'circle' ]`

Additional elements to draw.

Default: `false`


#### `keepRatio: true | [ 'axisX', 'axisY', 'bboxCorners', 'bboxSides' ] | false`

Scale axes together or individually.

Default: `false`


#### `range: { rotate: [ num, num ], scale: [ num, num ] }`

Limit the range of transformation.

Default: `{ rotate: [ -180, 180 ], scale: [ 0, 99999 ] }`


#### `rotate: true | [ 'axisX', 'axisY', 'self' ]|false`

Enables/disables rotating.

Default: `[ 'axisX', 'axisY' ]`


#### `scale: true | [ 'axisX', 'axisY', 'bboxCorners', 'bboxSides' ] | false`

Enables/disables scaling.

Default: `[ 'axisX', 'axisY', 'bboxCorners', 'bboxSides' ]`


#### `snap: { rotate: num, scale: num, drag: num }`: 

Snap transformations to num degrees (rotate) or pixels (scale, drag).

Default: `{ rotate: 0, scale: 0, drag: 0 }`


#### `snapDist: { rotate: num, scale: num, drag: num }`

Snap distance in degrees (rotate) or pixels (scale, drag).

Default: `{ rotate: 0, scale: 0, drag: 7 }`


#### `size: num | { axes: num, bboxCorners: num, bboxSides: num, center: num }`

Sets the radius of the handles in pixels.

Default: `5`


Callback
--------

A callback function can be specified to capture changes and events.


Functions
---------

#### `apply()`

Programmatically apply transformations (see the example above).


#### `hideHandles( opts )`

Removes handles but keeps values set by the plugin in memory. By
default removes all drag events from the elements. If you'd like to
keep then while the handles are hidden, pass ``{undrag: false}`` to
hideHandles().


#### `showHandles()`

Shows handles hidden with `hideHandles()`.


#### `setOpts( object, function )`

Update options and callback.


#### `unplug()`

Removes handles and deletes all values set by the plugin.


#### `updateHandles()`

Updates handles to reflect the element's transformations.

*Licensed under the [MIT license](http://www.opensource.org/licenses/mit-license.php).*
