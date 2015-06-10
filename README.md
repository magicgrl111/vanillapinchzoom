This is a fork of [Jordan Gensler's Vanilla Pinch NPM Package](https://www.npmjs.com/package/vanillapinch)
# VanillaPinchZoom

VanillaPinchZoom is a fork of PinchZoom.js with no jQuery dependency. The library provides multi touch gestures for zooming and dragging on any DOM element.

Finally, you are free of the shackles of jQuery! All you need is a [modern browser](http://caniuse.com/use-strict).

## Usage

The library exports a CommonJS module, and is designed for use with Browserify. For your conveience, a built version of VanillaPinchZoom is included in `dist/`, which is a standalone Browserify bundle that assigns `VanillaPinchZoom` on the global object.

```Javascript

var VanillaPinchZoom = require('vanillapinchzoom');

var myVanillaPinchZoom = new VanillaPinchZoom(document.querySelector('#your-element'), options);

```

### Options

```Text

tapZoomFactor:      The zoom factor a double tap zooms to. (default 2)
zoomOutFactor:      Resizes to original size when zoom factor is below the configured value. (default 1.3)
animationDuration:  The animation duration in milliseconds. (default 300)
maxZoom:            The maximum zoom factor. (default 4)
minZoom:            The minimum zoom factor. (default 0.5)
lockDragAxis        Locks panning of the element to a single axis. (default false)

```

# Events

Pinchzoom emits some custom events you can listen to

```Text

pz_zoomstart  Started to zoom
pz_zoomend    Stopped zooming
pz_dragstart  Started to drag the element
pz_dragend    Stopped to drag the element
pz_doubletap  Resetting the zoom with doubletab

```

### Methods

```Text

enable:             Enables all gesture capturing (default)
disable:            Disables all gesture capturing

```
