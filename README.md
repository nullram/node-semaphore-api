# semaphore-sms-api

Semaphore SMS API Client based on [homepage](http://semaphore.co/).



## Installation

	npm install semaphore-sms-api



You also need to provide your **API KEY** from Semaphore.

## Usage

	var Semaphore = require('semaphore-sms-api');

    var apikey = "YOUR_API_KEY";
	var sms = new Semaphore(apikey);

	// To check your account status:
    sms.account(function(error, result) {
    	if (!error)
    		console.log(result);
    });

    // To send a single SMS message:
    var payload = {
    	from: 'SEMAPHORE',
    	to: '09179008888',// To send in bulk '09xxxxxxxxx,09xxxxxxxxx'
    	message: 'Semaphore API Rocks!'
    };
    sms.sendsms(payload, function(error, result) {
    	if (!error) {
    		console.log(result);
    	} else
    		console.log(error);
    });    


## License

MIT

## Release History

* 1.0.0 - Initial release
