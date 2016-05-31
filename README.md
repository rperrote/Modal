# modal.js

> A modern and simple modal

[![npm][npm-image]][npm-url] [![license][license-image]][license-url]


**NPM**

```sh
npm install --save modal.js
```

**Download**

See https://necolas.github.io/normalize.css/latest/normalize.css


## What does it do?

* Build a modal customizable.
* By default create text, image modal.
* You can customize it with parameters
* Its possible to create different styles of the same modal and then choose one


## Browser support (Only tested on)

* Chrome (last two)
* Firefox (last two)



## Modal on!

#### Default mode

Not recommended! My use of styles is disgusting, You are warned! 

```javascript
$().modal({"content": {"type":"text","data": "Hola mundo!" }});
$().modal({"content": {"type":"image", "data": "http://lorempixel.com/400/200/"}})
```

#### Newbie mode

The parameter is json with this structure:

```javascript
'content' : {                    //<-- Content!
    'type' : String,             //<-- Type of data entry. Default: text. It must exist on plugin.json
    'data' : Object,             //<-- Any data to show. Here.
    'className' : String,        //<-- Name of class on css who define style of content.
},
'shape' : {                      //<-- Shape!
    'className' : String,        //<-- Name of class on css who define style of the shape literally*
    'style' : String             //<-- Name of class on css who define style of the canvas of content*
}
'layout' : String,               //<-- Define layout of modal*
'header' : {					 //<-- Header!
    'icon' : String,             //<-- If you wanna set a icon or a something on header but not content.
    'title' : {                  //<-- Title!
        'className' : String,    //<-- Name of class on css who define style of title header.
        'content' : String       //<-- Text of title
	}
},
'close' : {                      //<-- Close modal!
    'button' : Boolean,          //<-- True or empty or null create a close button. False dont.
    'escape' : Boolean           //<-- True or empty or null set key 'Esc' to close modal.
},
'acc' : {                        //<-- Accessibility time!
    'text' : String              //<-- Text to read for accessibility readers.
},
'btns' : [{                      //<-- Buttons everywhere! Is an array of buttons.
    'value' : String,            //<-- Text display on button.
    'shape' : String,            //<-- Name of class on css who define a style of button.
    'type' : String,             //<-- Define event of button. Function, link or close modal.
    'action' : String,           //<-- Define funcion or link of type button.
    'close' : Boolean,           //<-- True or empty or null button close modal. False dont.
    'key' : CharCode             //<-- Charcode of key trigger of btn.
}],
'overlay' : {                    //<-- Overlay!
    'className' : String,        //<-- Overwrite style of overlay.
    'click' : Boolean            //<-- True, empty or null close modal on click overlay. False dont.
},
'width' : String                 //<-- Set with of modal. Auto for default.
```

#### Pro mode

Adding `overflow: hidden` fixes IE9's SVG rendering. Earlier versions of IE
don't support SVG, so we can safely use the `:not()` and `:root` selectors that
modern browsers use in the default UA stylesheets to apply this style. [Source]
(https://lists.w3.org/Archives/Public/public-svg-wg/2008JulSep/0339.html).

#### God mode

By default, Chrome on OS X and Safari on OS X allow very limited styling of
`select`, unless a border property is set. The default font weight on `optgroup`
elements cannot safely be changed in Chrome on OSX and Safari on OS X.


## Acknowledgements

Normalize.css is a project by [Nicolas Gallagher](https://github.com/necolas),
co-created with [Jonathan Neal](https://github.com/jonathantneal).


[changelog-image]: https://img.shields.io/badge/changelog-md-blue.svg?style=flat-square
[changelog-url]: CHANGELOG.md
[license-image]: https://img.shields.io/npm/l/normalize.css.svg?style=flat-square
[license-url]: LICENSE.md
[npm-image]: https://img.shields.io/npm/v/normalize.css.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/normalize.css
[gitter-image]: https://img.shields.io/badge/chat-gitter-blue.svg?style=flat-square
[gitter-url]: https://gitter.im/necolas/normalize.css




