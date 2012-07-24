# OpenTok Plugin

## Description

Opentok is an API to stream live video to and from your App on mobile and on the web. [Find out more online](http://www.tokbox.com/opentok/api).

## Usage

To use the OpenTok Library, just include the OpenTok javascript file in your html file.

` <script src="OpenTok.js"></script> `

## TB Object
TB Object lets you initialize the OpenTok API and set up exception event handling.

In most cases, you would want to start with the TB Object

## Creating a Publisher Object

```javascript
var publisher = TB.initPublisher( apiKey:String [, replaceElementId:String] [, properties:Object] )
```

Initializes and returns a Publisher object. You can use this Publisher object to test the microphone and camera attached to the Publisher, and then pass this Publisher object to Session.publish() to publish a stream to a session.

### Parameters

**apikey** (String) - The API key that TokBox provided you when you registered for the OpenTok API.
**replaceElementId** (String) - Optional. The id attribute of the existing DOM element that the Publisher video replaces. If you do not specify a replaceElementId, the application appends a new DOM element to the HTML body. 

**properties** (Object) — Optional. This is an optional object that contains the following properties (each of which are optional):

* **cameraName** (String) - The preferred camera position. When setting this property, if the change is possible, the publisher will use the camera with the specified position.  
Valid Inputs: 'Front' or 'Back'
* **height** (Integer) — The desired height, in pixels, of the displayed Publisher video stream (default: 198). 
* **width** (Integer) — The desired width, in pixels, of the displayed Publisher video stream (default: 264). 
* **name** (String) — A string that will be associated with this publisher’s stream. This string is displayed at the bottom of publisher videos and at the bottom of subscriber videos associated with the published stream.
* **publishAudio** (Boolean) — Whether to publish audio.
* **publishVideo** (Boolean) — Whether to publish video.


### Return

**Publisher** — A Publisher object.


## Creating a Session Object
```javascript
var session = TB.initSession(sessionId:String)
```

Initializes and returns the local session object for a specified session ID.  
You connect to the session using the connect() method of the Session object returned by the TB.initSession() method. TB.initSession() does not initiate communications with the cloud, it simply initializes the Session object that you can use to connect (and to perform other operations once connected).

### Parameters

**sessionId** (String) — Use the [Session ID](http://www.tokbox.com/opentok/api/tools/js/documentation/overview/session_creation.html) generated by your server that represents the session to which you are planning to connect.

### Returns

**Session** — The session object through which all further interactions with the session will occur.



## Add Event Listener
```javascript
TB.initSession(type:String, listener:Function)
```

Registers a method as an event listener for a specific event. The TB class will dispatch exception events and error messages.

### Parameters

**type** (String) — This string identifying the type of event. The TB object can only dispatch one type of event: an exception event. The only valid input is 'exception'. Look at ExceptionEvent Class to learn more
**listener** (Function) - The function to be invoked when the TB object dispatches the event. A ExceptionEvent object will be passed into this function


## Learn More!
[Session Object](session.md)  
[Publisher Object](publisher.md)  
[Stream Object](stream.md)  
[Subscriber Object](subscriber.md)  
[ExceptionEvent Object](exceptionEvent.md)  
[Connection Object](connection.md)  


## License

Copyright (c) 2012 TokBox, Inc.
Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in 
the Software without restriction, including without limitation the rights to 
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies 
of the Software, and to permit persons to whom the Software is furnished to do 
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all 
copies or substantial portions of the Software.

The software complies with Terms of Service for the OpenTok platform described 
in http://www.tokbox.com/termsofservice

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR 
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, 
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE 
SOFTWARE.

