# dark-fomantic-ui

Adds Dark Theme selector and auto-detection logic to [Fomantic-UI](https://github.com/fomantic/fomantic-ui)

## Configuration

Just edit the following variables in `dark-fomantic-ui.js`:

```js
var $themeElements = [
	{ name: 'dividingHeaders', target: $('.ui.dividing.header').not('.inverted') },
	{ name: 'iconHeaders', target: $('.ui.icon.header').not('.inverted') },
	{ name: 'headers', target: $('.ui.header').not('.inverted') },
	{ name: 'forms', target: $('.ui.form').not('.inverted') },
	{ name: 'tooltippedIcons', target: $('.tooltipped.icon') },
	{ name: 'cardsContainer', target: $('.ui.cards') },
	{ name: 'cards', target: $('.ui.card') },
	{ name: 'dropdowns', target: $('.ui.dropdown') },
	{ name: 'fixedMenu', target: $('.ui.top.fixed.menu') },
	{ name: 'breadcrumb', target: $('.ui.breadcrumb') },
	{ name: 'accordions', target: $('.ui.accordion').not('.styled').not('.inverted') },
	{ name: 'tables', target: $('.ui.table') },
	{ name: 'segments', target: $('.ui.segment').not('.inverted') },
	{ name: 'placeholders', target: $('.ui.placeholder') }
];
var $themeValue = $('#theme-value');
var $darkThemeButton = $('div.right.menu div#dark-theme');
var $lightThemeButton = $('div.right.menu div#light-theme');
```

Where `$themeElements` array contains all DOM elements that will be styled and get the `inverted` class applied to.

Each elements objects have two properties:

1. `name`: Unique name to distinguish your DOM element
2. `target`: The target `jquery` DOM element

The other variables, `$themeValue`, `$darkThemeButton` and `$lightThemeButton` are used that way:

* `$themeValue`: DOM element where the current theme value will be written
* `$darkThemeButton`: DOM element that will activate the dark theme
* `$lightThemeButton`: DOM element that will activate the light theme

## Setup

To include the code in your project, simply add it after your [Fomantic UI](https://github.com/fomantic/fomantic-ui) inclusion line:

```html
...

<!-- Fomantic-UI -->
<script type="text/javascript" id="jquery-js" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.js" integrity="sha256-QWo7LDvxbWT2tbbQ97B53yJnYU3WhH/C8ycbRAkjPDc=" crossorigin="anonymous"></script>
<script type="text/javascript" id="fomantic-ui-js" src="https://cdnjs.cloudflare.com/ajax/libs/fomantic-ui/2.8.5/semantic.js" integrity="sha256-SeNU96at0t5XRuSk9/cLHWCGC0Ju5pug2NRGXeJCQN4=" crossorigin="anonymous"></script>

<!-- Including Dark Theme -->
<script type="text/javascript" id="dark-ui-js" src="dark-fomantic-ui.js"></script>
```

## Autodetection

The theme autodetection feature is based on [window.matchMedia](https://developer.mozilla.org/en/docs/Web/API/Window/matchMedia) and [prefers-color-scheme](https://developer.mozilla.org/en/docs/Web/CSS/@media/prefers-color-scheme).

## Screenshots

Here are some screenshots to show how to enable the __Dark Mode__.

### Activation buttons

Light:

![image](https://user-images.githubusercontent.com/9881407/92534300-b52bf700-f234-11ea-8c9a-e8961996ac39.png)

Dark:

![image](https://user-images.githubusercontent.com/9881407/92534459-1b187e80-f235-11ea-9bff-64b4bc66a408.png)

### Sample results

> From the [Nmap WebUI](https://github.com/Jiab77/nmap-webui) project.

Light theme:

![image](https://user-images.githubusercontent.com/9881407/92534621-8b270480-f235-11ea-9ef5-90410da21ea0.png)

Dark theme:

![image](https://user-images.githubusercontent.com/9881407/92534671-aa259680-f235-11ea-8b3e-82e224661df6.png)
