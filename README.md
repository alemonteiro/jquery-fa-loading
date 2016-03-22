# jQuery & Font Awesome Modal Loading

Simple jQuery plugin to add modal loading using Font Awesome spin icons.

Any of the Font Awesome icons can be used: https://fortawesome.github.io/Font-Awesome/icons/#spinner

Very simple and ugly demo page: http://alemonteiro.com.br/demos/fa-loading

## Usage

```
	var $el = $("body"); // or any relative, absolut or fixed positioned element
	
	// Add default loading
	$el.faLoading();

	// Add with options or update
	$el.faLoading(/*object*/options); // See list bellow

	// Remove loading
	$el.faLoading(false);
	// or
	$el.faLoading('remove');
	
	// Setting the loading icon
	$el.faLoading('fa-spinner');
	
	// To Update the Loading to a Succesfull or Failed status
	$el.faLoading("fail", "Message", "Title");
	$el.faLoading("success", "Message", "Title");

	// To change the default icon for all loadings
	$.faLoadingDefaultIcon = 'fa-cog';
	
```

## Options

```
var _defaults = {
	type: undefined 
		// type undefined/true/"add" will add loading 
		// type false/"remove" will remove loading
		// type "update" will update settings
	, title: undefined // creates an title bar
	, icon: "fa-refresh" //  fa icon
	, spin: false // icon sppining
	, status : "loading" // text message ( undefined or false for empty )
	, text : false   // text message ( undefined or false for empty )
	, timeout : undefined // timeout to close msg
	, closeCallback: undefined // call back for when the message is closed (by timeout or x button(in case it ever gets one))
	, closeButton: false // adds and close button
}
```

## CSS Customization

To change background and icon color you can override those css rules

```
.fa-loading-bg 
{
    background: rgba(0, 0, 0, 0.6); // modal background
}
.fa-loading-icon-wrapper .fa-loading-icon
{
    color: #000; // icon color
	font-size: 5em; // icon size 
	margin-top: -2.5em; // must be -50% of the font-size so it'll be always vertically centered
}
```

## Notes

It only works for elements that have relative, absolute, fixed or sticky positioning.


## Browser Compatibility

Tested ok on Firefox 45, Chrome 47 and Internet Explorer 11

## Changelog

### V 0.3 - 18/03/2016
```
Added updated method
Added default 'success' and 'fail' default updates
Added title property
```
### V 0.2 - 06/01/2016
```
Removed unnecessary methods and focused "all" functionality on 'faLoading' for better jQuery standarts
```