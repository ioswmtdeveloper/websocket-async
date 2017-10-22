<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [WebSocketClient](#websocketclient)
    -   [connected](#connected)
    -   [dataAvailable](#dataavailable)
    -   [connect](#connect)
    -   [send](#send)
    -   [receive](#receive)
    -   [disconnect](#disconnect)

## WebSocketClient

An asynchronous WebSocket client.

### connected

Whether a connection is currently active.

Returns **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

### dataAvailable

The number of messages available to receive.

Returns **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

### connect

Sets up a TCP connection to specified host and port. Resolves when the 
connection is established.
Can be called again to reconnect, to the same or even a different url.

**Parameters**

-   `url` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `protocols` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;void>** 

### send

Send data through the websocket.

**Parameters**

-   `data` **any** 

### receive

Asynchronously receive data from the websocket.
Resolves immediately if there is buffered, unreceived data.
Otherwise, resolves with the next rececived message, 
or rejects if disconnected.

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;any>** 

### disconnect

Initiates the close handshake if there is an active connection.
Returns a promise that will never reject.
The promise resolves once the WebSocket is closed.

**Parameters**

-   `code` **any** 
-   `reason` **any** 

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;[CloseEvent](https://developer.mozilla.org/en-US/docs/Web/API/CloseEvent)?>** 