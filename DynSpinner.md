DynSpinner {#DynSpinner}
======================================

Dynamic and customizable SVG or Canvas spinner overlay class.

DynSpinner Method: constructor {#DynSpinner:constructor}
------------------------------------------------------

### Syntax:

	DynSpinner.Canvas.Flower(target);
	DynSpinner.Canvas.Bubbles(target);
	DynSpinner.SVG.Flower(target);
	DynSpinner.SVG.Bubbles(target);

### Arguments:

1. target - (*element* or *id*) the overlayed element.
2. options - (*object* optional) see below.

### Options:

* nb_subdivision - (*integer*, defaults to `3`) Spinner's length in blocks. Should not work well with large values.
* duration - (*integer*, defaults to `250`) Duration of a single block (in milliseconds). Will change spinning speed.
* fps - (*integer*, defaults to `5`) Value passed to the blocks opacity fx effect.
* max_size - (*integer*, defaults to `0.6`) Maximum spinner size within the target element. Defaults to 60% (`0.6`).
* opacity - (*integer*, defaults to `0.8`) Spinner's overlay opacity value. Defaults to 80% (`0.8`).
* storage - (*element* or *id*) Spinner element storage. Defaults to document.body.
* rotation - (*integer*) Defaults to '1' clockwise. Set to '0' for counter-clockwise. 
* gradient - (*string* array) List of colors used for gradient filling
* stroke - (*string*) Stroke color
* spacing - (*real* 0..1) Space between elements, in element size. defaults to 0.25
* inner_ratio - (*real* 0..1) Size of the center hole. defaults to 0.2

### Returns:

(object) A new DynSpinner.SVG or DynSpinner.Canvas instance.

### Prerequisite:

CSS declarations

	.dynspinner_layer { background:#FFFFFF; } /* overlay */
	.dynspinner_container {}

### Example: 

	var spinner = new DynSpinner.Canvas.Bubbles('spinnable',
	{
		duration: 500, /* spin slower */
		fps: 50, /* Intensive but smoother transitions */
		max_size: 1.0 /* fill up entirely */
	});

	
DynSpinner Method: startSpin {#DynSpinner:startSpin}
--------------------------------------------------

Starts spinning. 

### Syntax:

	spinner.startSpin();


DynSpinner Method: stopSpin {#DynSpinner:stopSpin}
--------------------------------------------------

Stops the spinner. 

### Syntax:

	spinner.stopSpin();
	

DynSpinner Method: setTarget {#DynSpinner:setTarget}
--------------------------------------------------

Binds to and overlays another element.

### Syntax:

	spinner.setTarget('otherelement');
	
### Arguments:

1. target - (*element*) the new overlayed element.


DynSpinner Method: adaptSize {#DynSpinner:adaptSize}
--------------------------------------------------

Force recomputing spinner's sizings.

### Syntax:

	spinner.adaptSize();
