# Flexible squares

> *flexible and responsive squares for everyone!*

## Introducion

This is a little helper to build perfect flexible and responsive squares on your website. It works with pure css, less or scss.

Essentially, this thing here is nothing else then a grid system which is in shapes of squares. The reason why I made it anyway is simple: It’s a real pain to put seven squares (with a total width of 100%) in the bootstrap grid for example. **Therefore: Flexible & responsive squares!**

## Example

This example works with 10 rows. If you want another number of rows, just change the 10. The less file supports up to 12 rows. Feel free to add your custom number of rows to the file on your project.

```html
<div class="fs-cell fs-rows-10">
	<span class="fs-content">
		<!-- content goes here -->
	</span>
</div>

<!-- nine more div's like above are following here -->
```

```less
.fs-cell {
  float: left;
  position: relative;

  .fs-content {
    display: block;
    position: absolute;
  }

  &.fs-rows-10 {
    width: calc(100%/10);
    padding-bottom: calc(100%/10);
  }
}
```

## How it works

#### .fs-cell *- The actual grid-system*

The grid is a really simple calculation. Since we can use the calc() function in css, it's a one-liner: `width: calc(100%/10);` To get a square out of the div you can use the `padding-bottom` property. Also a one-liner: `padding-bottom: calc(100%/10);`  

**Important:** The second value in the calc() function is the grid count and must be the same on both properties!

- - -

#### .fs-content *- The content where you can do nearly everything ;)* 

The `position:absolute` on the content has it's right to exists. If you wouldn't do this, you won't get an exact square!

To position the content in the horizontal center, just add `right: 0; left: 0;` to the `<span>`. 

You want nice margins between the squares? The `.fs-content` element is the place to do this.

**Optional:**

*My initial idea was to build a simple color picker with pre-defined colors in form of a grid with squares.*
*With these Lines you get a 100% height and 100% width content `<span>` where you can put a background-color on it ;)*
```css
.fs-content {
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background: #212121;
}
```

## tl;dr

+ Put the less or css file into your project to build awesome flexible and responsive squares
+ Check this [fiddle](https://jsfiddle.net/jumpshoxx/pybhteu2/1/) to get an idea of the usage
+ This solution here isn't enough for you and don't fulfill your webdev dreams? Check this two projects here: http://www.fluidsquares.com/ | http://jsfiddle.net/webtiki/mpxyr/3/