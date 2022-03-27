# arduino_lib_ifttt  

A library to send trigger to an IFTTT webhook
(for the moment the implementation only supports ESP32)

## Usage  

* Define your IFTTT key (can be obtained at this link: https://ifttt.com/maker_webhooks/settings) and your event name
```
#define IFTTT_KEY  "YOUR_IFTTT_KEY"
#define IFTTT_EVENT_NAME "YOUR_EVENT_NAME""
```

* Instantiate a WiFiClientSecure object and pass it as parameter to the IFTTT object 
```
WiFiClientSecure client; 
IFTTT ifttt(IFTTT_KEY, client);
```

## Methods
 
* `Ifttt.triggerEvent(EVENT_NAME, value1, value2, value3)`  
Takes an Event Name and then you can optional pass in up to 3 extra Strings  
Returns true if successful
