FancySelect
===========

A non-obtrusive image dropdown menu that extends and replaces a standard HTML Select control.<br>
Requires Mootools Core 1.4.1 or later.

![Screenshot](https://github.com/lorenzos/FancySelect/raw/master/Graphics/logo.png)


How to use
----------

First of all, include in your page Mootools 1.4.1 or later, *FancySelect.js* source and *FancySelect.css* sheet.

	#HTML
	
	<script type="text/javascript" src="Mootools.js"></script>
	<script type="text/javascript" src="FancySelect.js"></script>
	<link type="text/css" href="FancySelect.css" rel="stylesheet">

Create a `<select>` element in HTML, and add a data-image 
attribute to `<option>`, specifing image paths:

	#HTML
	
	<select name="fruits" id="fruits">
		<option value="1" data-image="apple.png">Apple</option>
		<option value="2" data-image="banana.png">Banana</option>
		<option value="3" data-image="cherries.png">Cherries</option>
		...
	</select>

Then, in your Javascript:

	#JS
	
	$('fruits').fancySelect();

About **CSS styling**. The script comes with a sample CSS file.
You can easily change styles such as colors, backgrounds, borders, font 
and dimensions to customize FancySelect look, but be careful about the
layout properties - some of them are essential to make FancySelect works
as expected. 


Docs
----

**Implements:** Options, Events

**Syntax:**
	
	#JS
	
	var myFancySelect = new FancySelect(element, options);

- **element**: A `<select>` DOM element or ID.
- **options**: (*object*) Options for the class. They are all listed below.

**Options:**

- **showText**: If `TRUE` (default) keeps text in the dropdown menu.
- **showImages**: If `TRUE` (default) show images in the dropdown menu.
- **className**: A class name for CSS styling, default `'fancy-select'`.
- **autoHide**: If `TRUE` auto-hide the dropdown menu when user clicks outside.
- **autoScrollWindow**: If `TRUE` auto-scroll browser window when FancySelect is out of viewport.
- **animateFade**: If `TRUE` (default) animate the dropdown menu appearance.
- **fx**: An object for additional `Fx` options (default `{'duration': 'short'}`).

**Events:**

- **show**: The dropdown menu appears.
- **hide**: The dropdown menu disappears.
- **attach**: FancySelect just replaced the `<select>` DOM element.
- **detach**: The `<select>` DOM element is back.

**Methods:**

- **attach()**: Replace the `<select>` DOM element with FancySelect.
- **detach()**: Bring the `<select>` DOM element back.
- **select(value)**: Select a value.
- **show()**: Show the dropdown menu.
- **hide()**: Hide the dropdown menu.
- **toggle()**: Show/hide the dropdown menu.

**Element and Elements methods:**

You can use some shortcut methods on **Element** and **Elements** for creating and showing the FancySelect dropdown.

	#JS
	
	$$('select').fancySelect(options); // Attach FancySelect to all elements
	$('mySelect').fancySelectShow(); // Show the dropdown menu.
	var myFancySelect = $('mySelect').get('fancySelect'); // Get instance

- **Elements.fancySelect(options)**: Creates a new instance of FancySelect on elements.
- **Element.fancySelect(options)**: Creates a new instance of FancySelect on the element.
- **Element.fancySelectShow()**: Show the FancySelect dropdown on the element.
- **Element.fancySelectHide()**: Hide the FancySelect dropdown on the element.
- **Element.fancySelectToggle()**: Toggles the FancySelect dropdown on the element.
- **Element.get('fancySelect')**: Retrieves the FancySelect instance of the element.
