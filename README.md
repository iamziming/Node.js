#Node.js

<pre><code>
<h2>Day 1</h2>
var http = require("http");   //how we require modules

http.createServer(function(request, response){
	response.writeHead(200);  //status code in header
	response.write("Hello, this is dog.");  //response body
	response.end();  //close the connection - so the client on the other side knows it has received all the data.
}).listen(8080);  //listen for connections on this port

console.log("Listening on port 8080...");
</code></pre>

<pre><code>
<h2>Day 2 - Synchronous & Asynchronous</h2>
<h6>Synchronous Example</h6>
var myNumber = 1
function addOne() { myNumber++ } // define the function
addOne() // run the function
console.log(myNumber) // logs out 2

<h6>Asynchronous Example</h6>
var fs = require('fs') // require is a special function provided by node
var myNumber = undefined // we don't know what the number is yet since it is stored in a file

function addOne() {
  fs.readFile('number.txt', function doneReading(err, fileContents) {
    myNumber = parseInt(fileContents)
    myNumber++
  })
}

addOne()

console.log(myNumber) // logs out undefined -- this line gets run before readFile is done
</code></pre>
