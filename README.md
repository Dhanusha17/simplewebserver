# EX01 Developing a Simple Webserver
## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>TOP FIVE CRICKET PLAYERS IN THE WORLD</h1>
<h2>1. SACHIN TENDULKAR</h2>
<h2>2. VIVAN RICHARDS</h2>
<h2>3. SHANE WARNE</h2>
<h2>4. DALE STYEN</h2>
<h2>5. EOIN MORGAN</h2>
</body>
</html>
class MyServer(BaseHTTPRequestHandler):
def do_GET(self):
print("Get request received...")
self.send_response(200)
self.send_header("content-type", "text/html")
self.end_headers()
self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
## OUTPUT:
![311580826-5e538a7e-bd9d-490e-a775-9cf770d725e1](https://github.com/Dhanusha17/simplewebserver/assets/151549957/9a75c6a5-17c0-40c8-b538-11e887780658)


## RESULT:
The program for implementing simple webserver is executed successfully.
