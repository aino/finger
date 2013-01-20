Finger
======

Finger is a microweight swipe script that simulates native physics on touch devices.

There are no dependencies – you can use it as is without any library. There is no API or markup/CSS preferences, just a really small script that allows one child element to be swiped in pages based on it’s parent’s size.

It does not add swiping capabilities to mouse-based browsers, it only supports touch events.

We have focused on making the actual interaction as close as the native experience as possible, as well as providing a wide mobile browser support.

We use requestAnimationFrame for the optimal 60fps animation and integrated easing functions without resolving to CSS3 transitions that often distorts the interaction. We also use hardware transitions where possible and added a basic jQuery plugin in the core.

Usage
-----
	
	// using vanilla JS
    new Finger(document.getElementById('swipe'), options)

    // using jQuery
    $('swipe').finger(options)

Device support
--------------

Test suites right now includes:

* iPhone IOS 5+ Chrome & Safari
* iPad IOS 5+ Chrome & Safari
* Android 4.11+ Safari, Chrome, Opera & Firefox

We plan on including windows phone and older Android versions as soon as posslbe.

License & Demo
--------------

No MIT license yet, just GPL as we figure out what we will use this for...

See the included index.html for a simple demo.