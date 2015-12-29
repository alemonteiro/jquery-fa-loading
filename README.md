# jQuery Font Awesome Modal Loading

Simple jQuery plugin to add modal loading using Font Awesome spin icons.

Any of the Font Awesome spin icons can be used: https://fortawesome.github.io/Font-Awesome/icons/#spinner

Very simple and ugly demo page: http://alemonteiro.com.br/demos/fa-loading

## Usage

```
	// Adds loading and returns body
	$("body").faLoading(); 
	// Removes the loading and returns body
	$("body").faLoadingStop();
	
	// Adds loading and return the loading wrapper
	var $loading = $("body").faLoadingAdd(); 
	$loading.remove(); // remove the loading wrapper
	
	// To change the default icon for all loadings
	$.faLoadingDefaultIcon = 'fa-cog';
	
	// To change only for one loading
	$("body").faLoading('fa-spinner');
	
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