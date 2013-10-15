# jQuery ColorInput

The powerful jQuery plugin that for color picker. <a href="http://amazingsurge.github.io/jquery-colorInput/">Project page and demos</a><br />
Download: <a href="https://github.com/amazingSurge/jquery-colorInput/archive/master.zip">jquery-colorInput-master.zip</a>

***

## Features

* **beautiful skin** — we provide some beautiful skins, it also support custom skin.
* **support all color format** — hex rgb raba hsl hsla 
* **UX optimize** — we do a lot work to improve UX
* **Lightweight size** — 1 kb gzipped

## Dependencies
* <a href="http://jquery.com/" target="_blank">jQuery 1.83+</a>
* <a href="https://github.com/amazingSurge/jquery-color" target="_blank">jquery-color.js</a>

## Usage

Import this libraries:
* jQuery
* jquery-color.js
* jquery-popup.min.js

And CSS:
* colorInput.css 

Still don't forget include: image file

Create base html element:
```html
    <div class="example">
        <input type="text" class="colorInput" /> 
    </div>
```

Initialize tabs:
```javascript
$(".colorInput").colorInput();
```

Or initialize tabs with custom settings:
```javascript
$(".colorInput").colorInput({
	showInput: true,
	skin: 'simple'
});
```

## Settings

```javascript
{   

    // Optional property, Set a namespace for css class
    namespace: 'colorInput',
    
    //Optional property, choose the loaded skin
    skin: null,

    //Optional property, if 'none',we can close at once needn't to give time to render css3 transition
    readonly: 'none',

    //Optional property, if true , it will remove trigger components, and show color panel on the page when page loaded.
    flat: true,

    //Optional property, string, define the output color format on input element, not component element.
    format: 'hex',

    //Optional property, config every registered component using component name 
    components: {
    	check: {},
    	hue: {},
    	alpha: {}
    },

    //Optional property, trigger when color change 
    onChange: function() {},

    //Optional property, trigger when open colorInput pancel, flat type will never trigger this event
    onShow: function() {},

    //Optional property, trigger when close colorInput pancel, flat type will never trigger this event
    onClose: function() {},

    //Optional property, trigger when init
    onInit: function() {},

    //Optional property, trigger when a color is applied
    onApply: function() {},
}
```

## Public methods

jquery colorInput has different methods , we can use it as below :
```javascript
// show colorInput panel
$(".colorInput").colorInput("show");

// close colorInput panel
$(".colorInput").colorInput("close");

// apply selected color
$(".colorInput").colorInput("apply");

// cancel selceted color
$(".colorInput").colorInput("cancel");

// set colorInput to specified color
$(".colorInput").colorInput("set");

// get selected color
$("colorInput").colorInput("get");

// enable colorInput
$("colorInput").colorInput("enable");

// disable colorInput
$("colorInput").colorInput("disable");

// destroy colorInput
$("colorInput").colorInput("destroy");

```

## Event

* <code>colorInput::show</code>: trigger when show colorInput pancel, flat type will never trigger this event
* <code>colorInput::close</code>: trigger when close colorInput pancel, flat type will never trigger this event
* <code>colorInput::apply</code>: trigger when a color is applied
* <code>colorInput::init</code>: trigger when init
* <code>colorInput::change</code>: trigger when color change

how to use event:
```javascript
$(document).on('colorInput::init', function(event,instance) {
    // instance means current colorInput instance 
    // some stuff
});
```

## Browser support
jquery-popup is verified to work in Internet Explorer 7+, Firefox 2+, Opera 9+, Google Chrome and Safari browsers. Should also work in many others.

## Changes

| Version | Notes                                                            |
|---------|------------------------------------------------------------------|
|   0.3.x | ([compare][compare-1.3]) add thumbnails function                    |
|   0.2.x | ([compare][compare-1.2]) add autoside function                    |
|   0.1.x | ([compare][compare-1.1]) add keyboard function                   |
|     ... | ...                                                              |

[compare-1.3]: https://github.com/amazingSurge/jquery-colorInput/compare/v1.3.0...v1.4.0
[compare-1.2]: https://github.com/amazingSurge/jquery-colorInput/compare/v1.2.0...v1.3.0
[compare-1.1]: https://github.com/amazingSurge/jquery-colorInput/compare/v1.1.0...v1.2.0

## Author
[amazingSurge](http://amazingSurge.com)

## License
jQuery-popup plugin is released under the <a href="https://github.com/amazingSurge/jquery-colorInput/blob/master/LICENCE.GPL" target="_blank">GPL licence</a>.


