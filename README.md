# pigpio-button

Button using npm module **pigpio**.

## Installation
	$ npm install pigpio-button --save

## Usage

````javascript
var Button = require('pigpio-button');

// Construct a new button. See source code for more options.
var button = new Button({pin:19});

button.on('click', (clicks, time) => {

    // clicks - number of clicks
    // time   - milliseconds since last button press

    if (clicks == 1) {
        if (time < 1000)
            console.log('Single click.');
        else
            console.log('Single long click.');
    }
    else {
        console.log('Double click (or more)');

    }
});
````
