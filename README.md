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

every file in node is considered as module

modules are not part of global// console.log(module)

jshint app.js

(function(exports, require, module, __filename, __dirname){}) // module wrapper function
there are built-in modules in node which we can found out in list of node docs

require('path') // node assumes it to be built-in module, otherwise it will look for relative path file
var pathObj = path.parse(__filename);

const os = require("os");
os.totalmem();
os.freemem();

const fs = require('fs');
const files = fs.readdirSync('./');
const files = fs.readdir('./', function(err, files){
    
});