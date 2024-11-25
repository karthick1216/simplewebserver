# EX01 Developing a Simple Webserver

# Date:25/11/2024
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
```

from http.server import HTTPServer, BaseHTTPRequestHandler
<!DOCTYPE html>
<head>
    <title>LAPTOP CONFIGURATION</title>
</head>

<body><center>
    <h1>Laptop's configuration</h1>KARTHICK<h1></h1></center>
    <table border="2px" align="center" cellpadding="10" style="background-color:rgb(0, 126, 128);" >
    <tr style="color: rgba(13, 15, 12, 0.263); ">
        <th>DEVICE SPECIFICATION</th>
        <th>DETAILS</th>
    </tr>
    <tr style="color:rgba(0, 0, 0, 0.623); ">
        <td>BRAND</td>
        <td>LENOVO</td>
    </tr>
    <tr>
        <td>MODEL NAME</td>
        <td>E16 GEN 4</td>
    </tr>
    <tr>
        <td>SCREEN SIZE</td>
        <td>15.6 inches</td>
    </tr>
    <tr>
        <td>COLOR</td>
        <td>BLACK</td>
    </tr>
    <tr>
        <td>RAM</td>
        <td>16GB</td>
    </tr>
    <tr>
      <td>ROM</td>
      <td>512GB</td>
    </tr>
    <tr>
        <td>HARD DISK</td>
        <td>CORE i5</td>
    </tr>
    <tr>
        <td>GRAPHICS CARD</td>
        <td>NVIDIA</td>
    </tr>
    <tr>
        <td>SYSTEM TYPE</td>
        <td>64 BIT-OS,X64</td>
    </tr>
</table>
<py-script>
 
</py-script>

</body> 
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


# OUTPUT:
![alt text](<Screenshot 2024-11-25 051306.png>)


# RESULT:
The program for implementing simple webserver is executed successfully.