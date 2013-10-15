Finger
======

Finger is a microweight swipe script that simulates native physics on touch devices.

As ever so often, we where looking around for a really simple script that does one thing right – enable swiping between pages or images with a true native "feel" to it. There are a lot of swipe scripts around, but most of them feel "off" when swiping and they often add unnecessary CSS rules, desktop browser support, APIs and other stuff that we can do ourself.

**Finger** adds page-flicking capability to any child element with a true native feel. There are no dependencies – you can use it as is without any library. There is no API or markup/CSS preferences, just a really small script that allows one child element to be swiped in pages based on it’s parent’s size.

It does not add swiping capabilities to mouse-based browsers, only touch events are supported.

We have focused on making the actual interaction as close as the native experience as possible, as well as providing a wide mobile browser support.

We use requestAnimationFrame for the optimal 60fps animation and integrated easing functions without resolving to CSS3 transitions that often distorts the interaction. We also use hardware transitions where possible and added a basic jQuery plugin in the core.

Usage
-----

Example markup:

    <div id="swipe">
      <div class="pages">
        <div class="page"></div>
        <div class="page"></div>
      </div>
    </div>

Initializing the script:

	// using vanilla JS
    new Finger(document.getElementById('swipe'), options)

    // using jQuery
    $('#swipe').finger(options)

Options
-------

Just a few:

* `start` - sets the starting index (default 0)
* `duration` - sets the animation duration in ms (default 240)
* `easing` - sets the animation easing function, defaults to easeOutQuart
* `onchange(index)` - callback that fires whenever a page is changed. `index` is the new page.
* `oncomplete(index)` - callback that fires whenever a new page is showing and the animation is complete. `index` is the new page.


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