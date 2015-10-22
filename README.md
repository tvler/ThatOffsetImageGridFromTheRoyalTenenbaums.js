# That Offset Image Grid From <br> The Royal Tenenbaums <br> . javascript

A brand-new javascript file for repeating an HTML element's background image in a manner such that there will always be a vertically and horizontally centered image, and adjacent columns will be vertically offset by exactly one-half of the image's height.

###[Download](https://github.com/tvler/ThatOffsetImageGridFromTheRoyalTenenbaums.js/blob/master/ThatOffsetImageGridFromTheRoyalTenenbaums.js) ([minified](https://github.com/tvler/ThatOffsetImageGridFromTheRoyalTenenbaums.js/blob/master/ThatOffsetImageGridFromTheRoyalTenenbaums.min.js))
#### View [webpage](http://tylerdeitz.co/ThatOffsetImageGridFromTheRoyalTenenbaums.js), [more samples](http://tylerdeitz.co/ThatOffsetImageGridFromTheRoyalTenenbaums.js/samples)

![offset grid example](https://github.com/tvler/ThatOffsetImageGridFromTheRoyalTenenbaums.js/blob/master/img/wes1-offsetexample.jpg)

## 3 Ways To Use
##### 1. HTML + inline URL
```html
<figure
  data-offset = 'wes1.jpg'
></figure>
```
##### 2. HTML + CSS URL

```css
figure{
  background:url('wes1.jpg')
}
```
```html
<figure
  data-offset
></figure>
```
##### 3. HTML + JSON
```html
<figure
  data-offset = '{
    "src"      : "wes1.jpg",
    "width"    : "20%",
    "maxWidth" : 200
  }'
></figure>
```
*Default values*
```javascript
_offsetImg.defaultValues = {
  "src"       : "",
  // String of the image's URL
  // (If not given, CSS URL will be used)

  "snap"      : false,
  // Changes width of image to create a whole number of columns, only respecting one min/max property

  "minWidth"  : 0,
  "maxWidth"  : "100%",
  "width"     : 0,
  "minHeight" : 0,
  "maxHeight" : "100%",
  "height"    : 0
  // Can be a number or string ending in 'px' or '%'
}
```

##2 Steps To Run
##### 1. Link the javascript file
```html
<script
  src="ThatOffsetImageGridFromTheRoyalTenenbaums.js"
></script>
```
*This creates the object ```_offsetImg```*
##### 2. Set an event to update the background
```javascript
_offsetImg.update()
// When a data-offset element resizes, it's background needs to update
```

*Example hook*
```javascript
window.onresize =
  _offsetImg.update;
```

##Settings
##### 1. Add or remove ```data-offset``` elements
```javascript
_offsetImg.init()
// Run this function after an element is added or removed
```

##### 2. Change [default values](https://github.com/tvler/ThatOffsetImageGridFromTheRoyalTenenbaums.js#3-html--json)
```javascript
_offsetImg.defaultValues
// The exposed object's properties can be modified, which may reduce overall markup in some situations
// If it's modified after DOMContentLoaded, run _offsetImg.init()
```
