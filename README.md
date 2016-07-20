# I started learning Node.js!


//Day 1
*var http = require("http");   //how we require modules

http.createServer(function(request, response){
	response.writeHead(200);  //status code in header
	response.write("Hello, this is dog.");  //response body
	response.end();  //close the connection - so the client on the other side knows it has received all the data.
}).listen(8080);  //listen for connections on this port

console.log("Listening on port 8080...");*

//Day 2 - Asynchronous
