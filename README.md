 [![Packagist](https://img.shields.io/badge/License-MIT-blue.svg)](http://flwebsites.biz/jAlert/#license)
 [![Codeship](https://img.shields.io/badge/Build-Passing-green.svg)]()
 [![npm](https://img.shields.io/badge/NPM-v4.5.1-blue.svg)](https://npmjs.com/package/jAlert)
 
jAlert v4
======
by Versatility Werks http://flwebsites.biz

![logo](http://flwebsites.biz/jAlert/index-assets/img/logo.png)

Demo & Detailed Docs
=======
http://flwebsites.biz/jAlert/
===

What is it?
=======
Simple jQuery (Modal | Popup | Lightbox | Alert) Plugin

Whether you call it a lightbox, modal, popup, or window, jAlert is an excellent replacement / alternative for Simple Modal, FancyBox, or Reveal.

Getting the files
=======
Using NPM:
```html
npm install jAlert
```

Setup
======
Include the CSS files from the folder in the head section:
```html
<link rel="stylesheet" href="jAlert-master/dist/jAlert.css">
```

Include the JS file from the folder before the `</body>`:
```html
<script src="jAlert-master/dist/jAlert.min.js"></script>
<script src="jAlert-master/dist/jAlert-functions.min.js"></script> <!-- COMPLETELY OPTIONAL -->
```

To use the 'data-jAlert' attributes, you must attach the handlers (must be re-attached for newly added dynamic content):
```html
<a href='#' data-jAlert data-title='New jAlert!' data-content='Great job!'>Click Me</a>
```
```javascript
$(function(){
  $.jAlert('attach');
});
```

### This is the default usage. Doesn't require jAlert-functions.js
```javascript   
  $.jAlert({ //this is the normal usage
    'title': 'Test',
    'content': 'Howdy',
    'theme': 'green',
    'size': 'xsm'
  });
```

### Quick Use (requires jAlert-functions.js!!!)
```javascript
  alert('hi'); //override is enabled by default 
```
Note: When you run alert() in your console, it works as expected but will return "undefined"...ignore that. It's just because the function doesn't return anything. Had to add this disclaimer because people got confused..lol..
```javascript
  successAlert('Success', 'You did it!'); //green alert
```
```javascript 
  errorAlert('Error', 'It didn\'t work!'); //red alert
```
```javascript 
  infoAlert('Info', 'Information!'); //blue alert
```
```javascript 
  warningAlert('Warning', 'Warning!'); //yellow alert
```
```javascript 
  blackAlert('Warning', 'Warning!'); //black alert (obviously)
```
```javascript 
  imageAlert('http://mydomain.com/myimg.jpg'); //optional second param is the image width (defaults to auto)
```
```javascript 
  videoAlert('http://youtube.com/viddk35k');
```
```javascript 
  ajaxAlert('http://mydomain.com/myfile.php'); //optional second param is onOpen callback which gets passed the instance of jAlert
```
```javascript 
  iframeAlert('http://mydomain.com'); //optional second param is height (defaults to fill the viewport height)
```
```javascript   
  confirm(function(){
    console.log('confirmed!');
  }, function(){
    console.log('denied');
  });
```
```javascript   
  $.fn.jAlert.defaults.backgroundColor = 'white'; //override a default setting
  
  $.fn.jAlert({ //same as $.jAlert when you're not passing an element - this alert will now have the white background color
    'title': 'Test',
    'content': 'Howdy',
    'theme': 'green',
    'size': 'xsm'
    //'backgroundColor': 'white' //you could also pass it here
  });
  
  $.fn.jAlert.defaults.backgroundColor = 'black'; //set it back to black
```
```javascript 
  $('.btn').alertOnClick({ //this function attaches an onclick handler to .btn and passes the options to jAlert
    'title': 'It worked!',
    'content': 'You clicked the button'
  });
```
```javascript   
  $.alertOnClick('.btn', { //this function attaches an onclick handler to the body for .btn and kicks off jAlert
    'title': 'Like magic',
    'content': 'You clicked the button that was dynamically added'
  });
```
```javascript   
  $.jAlert({ //creates a lightbox for the image - responsive and all
    'image': 'http://mysite.com/my-image.jpg'
  });
 ```
```javascript  
  $.jAlert({ //creates a lightbox for the video - responsive and all
    'video': 'http://youtube.com/dflskd'
  });
```
```javascript   
  $.jAlert({ //creates an alert that fills most of the height with a scrollable iframe
    'iframe': 'http://mysite.com'
  });
```
```javascript   
  $.jAlert({ //gets content from another file with $.get()
    'ajax': 'my-ajax-content.php'
  });
```


Dependencies
=======
jQuery 1.7+

License
=======
M.I.T.

Copyright (c) 2015 Versatility Werks

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: 

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software. 

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
