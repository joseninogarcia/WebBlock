###WebBlock jQuery Plugin

WebBlock jQuery Plugin was made for one of my project to display an alert just like other websites that shows an information from an event that has been triggered by the end user. The goal of the plugin is to help every web pages to show the important message or an alert that has been specifically displayed by an element. Let say you have a method that will return an error, then I think you have to use this plugin and will serve you without any hassle by displaying what you want. Basically this is the same as the blockui plugin but this one is more easier.

###Version
1.0

###Installation and Usage

####The jQuery Library and the web blocker library
Before you begin, you need to install the jQuery library into your HTML code. New versions will do.

```html
<script type="text/javascript" src="https://code.jquery.com/jquery-2.1.4.min.js"></script>
```

Next, place the web blocker plugin right after the jQuery library:

```html
<script type="text/javascript" src="path/js/WebBlock.js"></script>
```

####Create your own button

In this demonstration, I create a button that once I clicked this, it will show what you expect:

```html
 <input type="button" name="blocker" value="Start Blocking" id="blocker" />
```

####Use the plugin together with the identifier

```javascript
$(document).ready(function(){
  $("#blocker").click(function(){
        $.BlockHTML({
          message : $("div"),
          containerHeight: 250,
          containerWidth: 300,
          backColor: "light-blue",
          backgroundOpacity : .5
        });
  });
});
```

####Web Blocker Properties

Below are the properties of the web blocker. You can use them to change the properties of the blocker.

| Property Name        | Description        |
| ------------- |:-------------:|
| message     | This is where you place the output of the blocker. The moment you set a value for this then you can see the output. Example: message : $("#div") | 
| containerHeight      | Sets the height of the container for the output.      |
| containerWidth | Sets the width of the container for the output.       |
| backColor | There are 3 types of background colors for the background: (a) light-black (b) light-green (c) light-blue |
| backgroundOpacity | Change the opacity of the background. Value should be from .1 to .9 |

####Unblocking the web page

To unblock the user interface, you can attach it through an event handler either on document ready or from the markup. See below examples:

#####Markup

```html
 <input type="button" value="unblock" onclick="$.UnBlockHTML();" />
```

#####jQuery

```html
 $(document).ready(function () {
       $("#blocker").click(function () {
           $.BlockHTML({
               $.UnBlockHTML();
           });
       });
   });
```

####Browser Compatibility

All New Browsers only. It is not working in IE8 below.

