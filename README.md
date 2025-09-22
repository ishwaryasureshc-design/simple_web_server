# EX01 Developing a Simple Webserver

# Date:22-09-25
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```from http.server import HTTPServer,BaseHTTPRequestHandler
content='''<!DOCTYPE html>
<html lang ="en"
<head>
      <meta charset="UTF-8">
      <meta name="view import content="width=device-width,initial-scale=2>
      <title>laptop specification</title>
</head>
<body bgcolor="violet">
<b><h1 align='center'>laptop specification</h1><b>
<h1 align="center"><font color="green">(DEVICE SPECIFICATION)</font></h1>
<h2><li><font color="red">device name:</font><font color="pink">ishwarya2704</font></h2></li>
<h2><li><font color="red">processor:</font><font color="pink">13th gen intel(R core(TM)i5-1334U(1.30 GHz)</font></h2></li>
<h2><li><font color="red">installed RAM:</font><font  color="pink">8.00GB(7.65 GB usable)</font></h2></li>
<h2><li><font color="red">device ID:</font><font color="pink">007CA7ED-9771-4474-A53F-B1BFB8AC95BF</font></h2></li>
<h2><li><font color="red">product ID:</font><font color="pink">00342-21290-64348-AAOEM</font></h2></li>
<h2><li><font color="red">system type:</font><font color="pink">64-bit operating system,64-based processor</font></h2></li>
<body bg color="violet">
<h1 align="center"><font color="brown">(WINDOW SPECIFICATION)</font></h1>
<h2><li><font color="grey">edition:</font><font color="yellow">window 11 home</font></h2></li>
<h2><li><font color="grey">version:</font><font color="yellow">24H2</font></h2></li>
<h2><li><font color="grey">installed on:</font><font color="yellow">13-07-2025</font></h2></li>
<h2><li><font color="grey">os built:</font><font color="yellow">26100.6584</font></h2></li>
<h2><li><font color="grey">experience:</font><font color="yellow">window feaeture xperience pack 1000.26100.234.0 </font></h2></li>
</body>
</html>'''
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address=('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
# OUTPUT:
![alt text](<../../simple_web_server/Screenshot 2025-09-20 112129.png>)
![alt text](<../../simple_web_server/Screenshot 2025-09-20 220419.png>)
# RESULT:
The program for implementing simple webserver is executed successfully.

