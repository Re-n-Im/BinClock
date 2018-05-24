# Binary Clock

A simple script for binary clock, impressed by KDE's applet

## Description

The script is written in JavaScript. It provides a few methods for interaction, as explained below.

## How to use it

It is necessary to use except the script, also and stylesheet to visualize the "clock" elements.
```HTML
<link rel="stylesheet" type="text/css" href="binClock.css">
<script src="binClock.js" type="text/javascript"></script>
```
To create a new binary clock, you need to call
```JavaScript
new BinaryClock( );
```
after the DOM tree has been loaded. `BinaryClock` accepts one parameter, which pass through `querySelector` or `getElementById`. Example:
```JavaScript
new BinaryClock( 'body' );
```
With chis code, the clock is created and visible, but it doesn't run.  
Here is an example:
```HTML
new BinaryClock( 'body' ).run( );
```

## Interface

### *`run()`*
**Info**: This method starts the engine of the clock  
**Arguments**: N/A
### *`stop()`*
**Info**: This method stops the clock  
**Arguments**: N/A
### *`showSeconds()`*
**Info**: This method makes the seconds elements visible  
**Arguments**: N/A
### *`hideSeconds()`*
**Info**: This method makes the seconds elements invisible  
**Arguments**: N/A
### *`setOrientation()`*
**Info**: This method sets the clock orientation  
**Arguments**:

1. **Orientation**
	* **Type**: String
	* **Value** - should be one of the following:
		* **btt** - bottom to top;
		* **ttb** - top to bottom;
		* **ltr** - left to right;
		* **rtl** - right to left;
		* **vertical** - same as **btt**;
		* **horizontal** - same as **rtl**.

### *`setSecondsPosition()`*
**Info**: This method sets the seconds block position  
**Arguments**:

1. **Position**
	* **Type**: String
	* **Value** - should be one of the following:
		* **center** or **middle** - the seconds will appear between the hours and the minutes blocks;
		* **end** or **side** - the seconds will appear at the end of the clock container, depending on chosen orientation.

### *`setType()`*
**Info**: This method sets the the type of the clock - 4 or 7 bit, i.e. to be presented each digit from clock's elements or the whole block of the clock elements  
**Arguments**:

1. **Type**
	* **Type**: String
	* **Value** - should be one of the following:
		* **wide**, **long** or **big** - for 7bit clock;
		* **tight**, **short** or **small** - for 4bit clock.

### *`setTheme()`*
**Info**: This method changes the theme of the clock (changes the css class)
**Arguments**:

1. **Theme**
	* **Type**: String
	* **Value** - CSS classname

### *`appendTo()`*
**Info**: This method appends the clock to a DOM element  
**Arguments**:

1. **Selector or DOM Element to append to**
	* **Type**: String
	* **Value** - should be CSS selector or DOM id attribute of element.

Example:
```JavaScript
new BinaryClock( )
.appendTo( 'body' )
.run( );
```

### Note
All of the above methods returns pointer to the created BinaryClock object; All of the above methods, except `run()` and `stop()`, are redrawing the clock container, regarding the new options.  

## Examples:
In [JSfiddle](https://jsfiddle.net/h6m4jvrs/2/):
```JavaScript
new BinaryClock( 'body' )
.setSecondsPosition( 'middle' )
.setType( 'small' )
.setOrientation( 'ttb' );
```
## Captures
|  | Example 1 | Example 2 | Example 3 | Example 4 |
| ------------ | ------------- | ------------ | ------------- | ------------ |
| Preview | ![Example](https://raw.githubusercontent.com/Re-n-Im/BinClock/5a80d6bb3f4b6a49380bc870d7b4fc23263ad8e4/img/example.png) | ![Example](https://raw.githubusercontent.com/Re-n-Im/BinClock/5a80d6bb3f4b6a49380bc870d7b4fc23263ad8e4/img/example2.png) | ![Example](https://raw.githubusercontent.com/Re-n-Im/BinClock/5a80d6bb3f4b6a49380bc870d7b4fc23263ad8e4/img/example3.png) | ![Example](https://raw.githubusercontent.com/Re-n-Im/BinClock/5a80d6bb3f4b6a49380bc870d7b4fc23263ad8e4/img/example4.png) |
