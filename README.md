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
* By default create text , image and video modal Youtube .
* Your personalized with params .
* Its possible to create different styles of the same modal and then choose one


## Browser support (Only tested on)

* Chrome (last two)
* Firefox (last two)


## Modal on!

#### `Default mode`

Not recommended! My use of styles is disgusting, You are warned! 

```javascript
$().modal({"content": {"type":"text","data": "Hola mundo!" }});
$().modal({"content": {"type":"image", "data": "http://lorempixel.com/400/200/"}})
```


#### `Newbie mode`

```javascript
'content' : {
		'type' : String,
		'data' : Object,
		'className' : String,
	},
	'shape' : {
		'className' : String,
		'style' : String
	}
	'type' : String,
	'header' : {
		'icon' : String,
		'title' : {
			'className' : String,
			'content' : String
		}
	},
	'close' : {
		'button' : Boolean,
		'escape' : Boolean
	},
	'acc' : {
		'text' : String
	},
	'btns' : [{
		'value' : String,
		'className' : String,
		'shape' : String,
		'type' : String,
		'action' : String,
		'close' : Boolean,
		'key' : String
	}],
	'overlay' : {
		'className' : String,
		'click' : Boolean
	},
	'width' : String
    ```

#### `Pro mode`

Adding `overflow: hidden` fixes IE9's SVG rendering. Earlier versions of IE
don't support SVG, so we can safely use the `:not()` and `:root` selectors that
modern browsers use in the default UA stylesheets to apply this style. [Source]
(https://lists.w3.org/Archives/Public/public-svg-wg/2008JulSep/0339.html).

#### `God mode`

By default, Chrome on OS X and Safari on OS X allow very limited styling of
`select`, unless a border property is set. The default font weight on `optgroup`
elements cannot safely be changed in Chrome on OSX and Safari on OS X.

#### `[type="checkbox"]`

It is recommended that you do not style checkbox and radio inputs as Firefox's
implementation does not respect box-sizing, padding, or width.

#### `[type="number"]`

Certain font size values applied to number inputs cause the cursor style of the
decrement button to change from `default` to `text`.

#### `[type="search"]`

The search input is not fully stylable by default. In Chrome and Safari on
OSX/iOS you can't control `font`, `padding`, `border`, or `background`. In
Chrome and Safari on Windows you can't control `border` properly. It will apply
`border-width` but will only show a border color (which cannot be controlled)
for the outer 1px of that border. Applying `-webkit-appearance: textfield`
addresses these issues without removing the benefits of search inputs (e.g.
showing past searches). Safari (but not Chrome) will clip the cancel button on
when it has padding (and `textfield` appearance).


## Contributing

Please read the [contribution guidelines](CONTRIBUTING.md) in order to make the
contribution process easy and effective for everyone involved.


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




