# Developing a Simple Webserver

# AIM:
NAME :PRAVEEN S
REFERENCE : 22009017

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
<title>
 Top five web application development frameworks:
</title>
</head>
<body>
<h1>Top five web application development frameworks:</h1>
<h1>js</h1>
<h1> Ember.js </h1>
<h1> Laravel </h1>
<h1> Ruby on Rails and Vue. js</h1>
<h1> Java Spring Framework </h1>
</body>
</html>
"""
  
class myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header("content-type", 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


Server_address =('',80)
httpd= HTTPServer(Server_address,myserver)
httpd.serve_forever()

```



# OUTPUT:
![eig](ss.png)

# RESULT:

The program is executed succesfully
