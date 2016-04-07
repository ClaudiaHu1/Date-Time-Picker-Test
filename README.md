# apm-date-time-picker

apm-date-time-picker enables setting a range of time using a calendar-based UI.

## Overview

Use the apm-date-picker to add a web component to your application enabling users to choose a start date-time and an end date-time. A graphical calendar UI with single calendars is presented, as well as a time range selector below the calendars.

## Usage

### Prerequisites

1. node.js
2. npm
3. bower
4. [webcomponents-lite.js polyfill](https://github.com/webcomponents/webcomponentsjs)

Node, npm and bower are necessary to install the component and dependencies. webcomponents.js adds support for web components and custom elements to your application.

### Getting Started

First, install the component via bower on the command line.

```
bower install https://github.com/PredixDev/date-time-picker-test.git --save
```

Second, import the component to your application with the following tag in your head.

```html
<link rel="import" href="/bower_components/date-time-picker-test/apm-date-picker.html.html" ></link>
```

Finally, use the component in your application:

```html
<apm-date-time-picker></apm-date-time-picker>
```

<br />
<hr />

## Attributes

#### selected-date-Time

*Type:* **Object** - (*Optional*) - *Default:* The previous week

The `selected-date-Time` attribute is 2-way data-bindable object with one properties. The value of these must be set to valid [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) date-time strings.

```html
<apm-date-time-picker
	...
	selected-date-Time="{{sampleData.selectedDateTime}}"
	>
</apm-date-time-picker>
```

#### allow-future-dates

*Type:* **Boolean** - (*Optional*) - *Default:* false

By default future dates are disabled in the date picker. Set the `allow-future-dates` attribute to "true" to enable future dates in the date range picker. *Note: No validation of dates is performed so users are able to enter manually any date without restriction. This attribute merely disables choosing future dates via the calendar UI.*

```html
<apm-date-time-picker
	...
	allow-future-dates="true">
</apm-date-time-picker>
```

#### display-options

*Type:* **Object** - (*Optional*) - *Default:* { "displayType": "normal", "submitButtonText": "Submit", "submitButtonIcon": "" }

Display configuration that enables customization of the `displayType`, `submitButtonText`, and `submitButtonIcon`.

```html
<apm-date-time-picker
	...
	display-options="{
        "displayType": "normal",
        "submitButtonText": "Submit",
        "submitButtonIcon": ""
    }">
</apm-date-time-picker>
```

<br />
<hr />

##Events
### `date-changed`
 *Note: The value will be automatically updated if you are using 2-way data-binding, making event listeners unnecessary.*

Attach an event listener using `addEventListener` like this:

```html
<apm-date-time-picker id="my-date-picker"></apm-date-time-picker>
```
```javascript
	var el = document.querySelector("#my-date-picker");
	el.addEventListener("date-changed", function(e) {
		// do something on date-changed
	});
```

## Using Events

Events follow the [Polymer data-binding standards](https://www.polymer-project.org/1.0/docs/devguide/data-binding.html).

You can can attach listeners by using one of the methods below:

1. Polymer Event listener
2. "on-x" annotated event listener
3. addEventListener vanilla Javascript method
<br />
<hr />

## Local Development

From the component's directory...

```
$ npm install
$ bower install
$ grunt sass
```

From the component's directory, to start a local server run:

```
$ grunt depserve
```

Navigate to the root of that server (e.g. http://localhost:8080/) in a browser to open the API documentation page, with link to the "Demo" / working examples.

### LiveReload

By default grunt watch is configured to enable LiveReload and will be watching for modifications in your root directory as well as `/css`.

Your browser will also need to have the LiveReload extension installed and enabled. For instructions on how to do this please refer to: [livereload.com/extensions/](http://livereload.com/extensions/).

Disable LiveReload by removing the `livereload` key from the configuration object or explicitly setting it to false.


### DevMode
Devmode runs `grunt depserve` and `grunt watch` concurrently so that when you make a change to your source files and save them, your preview will be updated in any browsers you have opened and turned on LiveReload.
From the component's directory run:

```
$ grunt devmode
```

### GE Coding Style Guide
[GE JS Developer's Guide](https://github.com/GeneralElectric/javascript)

<br />
<hr />

## Known Issues

Please use [Github Issues](https://github.com/PredixDev/COMPONENT/issues) to submit any bugs you might find.
# date-time-picker-px-test
