# swaggerDocGen

swagDocs/bootprint/target has the html and css documentation generated using the command line boot print tool. HTML file can just be opened using a browser.

swagDocs/swaggerUI/Dist has the html and css generated using the swaggerUI tool. The html must be served up. 
For example, using command line navigate to the dist folder. 
Run $ python -m SimpleHTTPServer 8080
go to localhost:8080 in browser to see the results. 

swagDocs/slate has the markdown used to generate html and css using slate. To run install slate. Replace the file included with slate at the location source/index.html.md with file from swagDocs/slate/index.html.md from this repo. Host with middleman or vagrant to view sample.
