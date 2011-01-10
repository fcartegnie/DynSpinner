DynSpinner
===========

![Screenshot](http://fcartegnie.github.com/DynSpinner/dynspinner.png)

DynSpinner is an expanding and customizable Canvas or SVG spinner overlay.

How to Use
----------

Add and the required css declarations

	.dynspin_layer { background:#FFFFFF; }
	.dynspin_container {}

Then just create an Instance on the target element

	#JS
	var spinner = new DynSpinner.Canvas.Bubbles('spinnable');
	spinner.startSpin();

The spinner can be rebound to another element at anytime

	#JS
	spinner.setTarget('otherspinnable');
