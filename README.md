# nodeproj1

Browser consists of javascript engine which takes javascript code and converts into machine code
IE --> Chakra
Firefox --> SpiderMonkey
Chrome --> V8(FASTEST)

bacause different engine javascript code behaves differently in different browser, browser provides runtime environment for javascript code

Node.exe --> V8 engine inside C++ program, don't have document object, JS engine + modules that gives us capability not available in browsers like filesystem and network

Node is not a framework its a runtime environment for javascript

Non-blocking/Asynchronous --> single thread handle multiple request

Node applications are asynchronous by default

single thread will process request and once the response is back from DB, it will put it in Event Queue, node will continously monitoring the queue, one it finds any event it will take it out and process it

ideal for I/O intensive apps and should not be used for CPU intensive application as it is single threaded, process one request at a time, only for data intensive and real time 

global is there in place of document and console.log can be accessed by global.console.log() but the variable and functions cannot be accessed using global they are undefined as they are scoped only to the file as per node modules
