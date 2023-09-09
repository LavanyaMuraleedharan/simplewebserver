# Developing a Simple Webserver
## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation
### Step 2:
Design of webserver workflow
### Step 3:
Implementation using Python code
### Step 4:
Serving the HTML pages.
### Step 5:
Testing the webserver

## PROGRAM:
```
NAME:LAVANYA M
REG NO:212222110021
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h2 align="center">Top 5 revenue companies </h2>
<hr>
<ol>
<h3>
<li>apple</li>
<li>amazon</li>
<li>Microsoft</li>
<li>alphabet</li>
<li>meta</li>
</h3>
</ol>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:
![Screenshot from 2023-09-09 09-20-09](https://github.com/LavanyaMuraleedharan/simplewebserver/assets/120103862/fc168291-398d-497c-9f0a-41494f070724)



## RESULT:
The program for implementing simple webserver is executed successfully.
