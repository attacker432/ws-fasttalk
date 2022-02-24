# ws-fasttalk
Simple code to make ws messages much faster.
```
const protocol = require('./fasttalk.js');
```
You can use ```protocol.encode``` when you send a message.
and you can use ```protocol.decode``` to decode a message that is sent to you.
```
 socket.talk = (...message) => {
 if (socket.readyState === socket.OPEN) { 
   socket.send(protocol.encode(message), { binary: true, }); 
} 
};
 ```
