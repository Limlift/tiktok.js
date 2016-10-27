# tiktok
This is a responsive jQuery Tip Plugin.
It's written to help me which I always have to rewrite tooltip or alertbox etc.<br>
It's base on another jQuery plugin [tioso.js](https://github.com/object505/tipso) .

## Getting started.
1. Include jQuery

	```html
	<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
	```

	>Requires jQuery 1.7+

2. Include plugin's code

	```html
	<link rel="stylesheet" href="/your_path/tiptok.css">
	<script type="text/javascript" src="/your_path/tiktok.js"></script>
	```

3. Call the plugin

	```js
	$(element).tiktok();
	```

## Usage.


```js
jQuery(element).tiktok({
	animateSpeed: 400, //Animate speed
	delay: 200, //Animate delay
	themeColor  :'#0082e5',//Theme bolor
	titleColor : '#0082e5',//Title bar bolor
	status : 'default',//Type of floattip:done/alert/error/default.
	position : null,//Position,for floattip type(top/left/right/down) and poptip type(top/middle/bottom)
	type : 'popbox',//Type of tip(popbox/poptext/popload/floattip/poptip)
	content : {
		'title':null,//Title of tips
		'content':null,//Content of tips
		'picurl':null//Pic of loaded tips
	},
	buttonCancel: 'CANCEL', //Text of cancel Button
	buttonConfirm: 'OK', //Text of confirm Button
	headerAlign : 'center',//Align of title
	contentAlign : 'left',//Align of content
	ajaxContentUrl: null, //Url of ajax request
	onConfirm:null,//Function to be executed after confirm button is clicked.
	onCancel:null,//Function to be executed after cancel button is clicked.
	onBeforeShow: null,//Function to be executed before tiktok is shown.
    onBeforeHide: null,//Function to be executed before tiktok is hidden.
	onShow: null,//Function to be executed after tiktok is shown.
	onHide: null//Function to be executed after tiktok is hidden.
})
```

## API.

```js
    // Show the tiktok tooltip
    $('.tiktok').tiktok('show');

    // Hide the tiktok tooltip
    $('.tiktok').tiktok('hide');

    // Destroy tiktok tooltip
    $('.tiktok').tiktok('destroy');

    // Add a callback before confirm button is clicked.
    $('.tiktok').tiktok({
        onConfirm: function ($element, element) {
            // Your code
        }
    });

    // Add a callback before cancel button is clicked.
    $('.tiktok').tiktok({
        onCancel: function ($element, element) {
            // Your code
        }
    });

    // Add a callback before tiktok is shown
    $('.tiktok').tiktok({
        onBeforeShow: function ($element, element) {
            // Your code
        }
    });

    // Add a callback when tiktok is shown
    $('.tiktok').tiktok({
        onShow: function ($element, element) {
            // Your code
        }
    });

    // Add a callback when tiktok is hidden
    $('.tiktok').tiktok({
        onHide: function ($element, element) {
            // Your code
        }
    });

    // Load AJAX content to tiktok
    $('.tiktok').tiktok({ 
        ajaxContentUrl : 'ajax.html'
    });

    // Update tiktok options
    $('.tiktok').tiktok('update', 'content', 'new content');
```

## License 

tiktok.js is licensed undet the MIT license.
