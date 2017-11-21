# pigpio-button

Button using module pigpio.

## Installation
	$ npm install pigpio-button --save

## Usage

````javascript
var Button = require('pigpio-button');
var button = new Button({pin:19});

button.on('click', (clicks, time) => {

    // clicks - number of clicks
    // time   - milliseconds since first button press

    if (clicks == 1) {
        console.log('Single click.');
    }
    else {
        console.log('Double click (or more)');

    }
});
````
