# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```python
DEVELOPED BY : JAYABHARATHI . S
REGISTER NO : 212222100013

from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<!DOCTYPE html>
<html>
<head>
<titlt>MY WEBSERVER</title>
</head>
<body>
<h1>top five web application development frameworks.
</h1>
<li>DJANGO</li>
<li>MEAN</li>
<li>MERN</li>
<li>SPRING BOARD</li>
<li>ASP.NET</li>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request recieved")
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
print("my webserver is running.....")
httpd.serve_forever()

```

## OUTPUT:

## SERVER OUTPUT
![image](https://user-images.githubusercontent.com/120367796/233161914-ee529076-3536-4c06-9d45-3457421aa8e2.png)

## CLIENT OUTPUT
![image](https://user-images.githubusercontent.com/120367796/227995572-ec38299b-16ec-4aba-aec7-ab2b5f8555d1.png)



## RESULT:
The program is executed succesfully
