CordovaKeyboard
======

> The `CordovaKeyboard` object provides some functions to customize the iOS keyboard.

This plugin has only been tested in Cordova 3.2 or greater, and its use in previous Cordova versions is not recommended (potential conflict with keyboard customization code present in the core in previous Cordova versions). 

If you do use this plugin in an older Cordova version (again, not recommended), you have to make sure the HideKeyboardFormAccessoryBar and KeyboardShrinksView preference values are *always* false, and only use the API functions to turn things on/off.

This plugin supports the __HideKeyboardFormAccessoryBar__ (boolean) and __KeyboardShrinksView__ (boolean) preferences in config.xml.

Methods
-------

- CordovaKeyboard.shrinkView
- CordovaKeyboard.hideFormAccessoryBar
- CordovaKeyboard.disableScrollingInShrinkView

Properties
--------

- CordovaKeyboard.isVisible

Events
--------

- CordovaKeyboard.onshow
- CordovaKeyboard.onhide
- CordovaKeyboard.onshowing
- CordovaKeyboard.onhiding


Permissions
-----------

#### config.xml

            <feature name="CordovaKeyboard">
                <param name="ios-package" value="CDVKeyboard" onload="true" />
            </feature>

CordovaKeyboard.shrinkView
=================

Shrink the WebView when the keyboard comes up.

    CordovaKeyboard.shrinkView(true);

Description
-----------

Set to true to shrink the WebView when the keyboard comes up. The WebView shrinks instead of the viewport shrinking and the page scrollable. This applies to apps that position their elements relative to the bottom of the WebView. This is the default behaviour on Android, and makes a lot of sense when building apps as opposed to webpages.


Supported Platforms
-------------------

- iOS

Quick Example
-------------

    CordovaKeyboard.shrinkView(true);
    CordovaKeyboard.shrinkView(false);

CordovaKeyboard.hideFormAccessoryBar
=================

Hide the keyboard toolbar.

    CordovaKeyboard.hideFormAccessoryBar(true);

Description
-----------

Set to true to hide the additional toolbar that is on top of the keyboard. This toolbar features the Prev, Next, and Done buttons.


Supported Platforms
-------------------

- iOS

Quick Example
-------------

    CordovaKeyboard.hideFormAccessoryBar(true);
    CordovaKeyboard.hideFormAccessoryBar(false);


CordovaKeyboard.disableScrollingInShrinkView
=================

Disable scrolling when the the WebView is shrunk.

    CordovaKeyboard.disableScrollingInShrinkView(true);

Description
-----------

Set to true to disable scrolling when the WebView is shrunk.


Supported Platforms
-------------------

- iOS

Quick Example
-------------

    CordovaKeyboard.disableScrollingInShrinkView(true);
    CordovaKeyboard.disableScrollingInShrinkView(false);

CordovaKeyboard.isVisible
=================

Determine if the keyboard is visible.

    if (CordovaKeyboard.isVisible) {
        // do something
    }

Description
-----------

Read this property to determine if the keyboard is visible.


Supported Platforms
-------------------

- iOS

CordovaKeyboard.automaticScrollToTopOnHiding
=================

Specifies whenether content of page would be autoamtically scrolled to the top of the page
when keyboard is hiding.

    CordovaKeyboard.automaticScrollToTopOnHiding = true;

Description
-----------

Set this to true if you need that page scroll to beginning when keyboard is hiding.
This is allows to fix issue with elements declared with position: fixed,
after keyboard is hiding.


Supported Platforms
-------------------

- iOS

CordovaKeyboard.onshow
=================

If defined, this function fired when keyboard fully shown.

    CordovaKeyboard.onshow = function () {
        // Describe your logic which will be run each time keyboard is shown.
    }

Description
-----------

Attach handler to this event to be able to receive notification when keyboard is shown.


Supported Platforms
-------------------

- iOS

CordovaKeyboard.onhide
=================

If defined, this function fired when keyboard fully closed.

    CordovaKeyboard.onhide = function () {
        // Describe your logic which will be run each time keyboard is closed.
    }

Description
-----------

Attach handler to this event to be able to receive notification when keyboard is closed.


Supported Platforms
-------------------

- iOS

CordovaKeyboard.onshowing
=================

If defined, this function fired before keyboard will be shown.

    CordovaKeyboard.onshowing = function () {
        // Describe your logic which will be run each time when keyboard is about to be shown.
    }

Description
-----------

Attach handler to this event to be able to receive notification when keyboard is about to be shown on the screen.


Supported Platforms
-------------------

- iOS

CordovaKeyboard.onhiding
=================

If defined, this function fired when keyboard fully closed.

    CordovaKeyboard.onhiding = function () {
        // Describe your logic which will be run each time when keyboard is about to be closed.
    }

Description
-----------

Attach handler to this event to be able to receive notification when keyboard is about to be closed.


Supported Platforms
-------------------

- iOS

