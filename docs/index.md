[OAD(./docs/home.yml)]

<!-- Convert the aboove .yml to .md file : oad gen-docs -s example1-openapi.yml/.json -d output.md 
This requires to install a module 'essentials-openapi' using pip [pip install essentials-openapi[full]] -->
## HTTP Status Code
### 2xx: Success
|   Status Code |   Body   | Usecase
| ------ | --------------------- | --------- | 
| <font color='green'> **200 OK**</font> | `{ "message": "Success" }` | The web page was Successfully loaded (`GET` request) | 
| <font color='green'> **201 Created**</font>       | `{ "message": "xxxxxxxx content created"}`  | Content was successfully created( `POST` request)  |
| <font color='green'> **204 No Content**</font>    | `{ "message": "No additional content"}`  | Request was successful, but no additional content (response body is not necessary).|
    

### 3xx: Redirection
|   Status Code | Body | Usecase |
| --------------| ---------|----------|
| <font color='blue'> **302 Found**</font> | `{ "message": "Resource found" }` | Requested resource resides temporarily under a different URL (temporary redirect).|
| <font color='blue'> **304 Not Modified**</font> |  `{ "message": "Not modified" }`  | Resource hasn't been modified since the last request.  |

### 4xx: Client Error
|   Status Code | Body | Usecase |
| --------------| ---------|----------|
| <font color='red'> **400 Bad Request**</font> |  `{ "message": "Invalid request" }`| Server cannot process the request due to client error  |
| <font color='red'> **401 Unauthorized**</font> | `{ "message": "Authentication required" }`| Requires user authentication|
| <font color='red'> **403 Forbidden**</font> | `{ "message": "Access denied" }` | Understood the request, but refuses to authorize it. |
| <font color='red'> **404 Not Found**</font> | `{ "message": "Resource not found" }` | Server can't find the requested resource |
| <font color='red'> **405 Method Not Allowed**</font> | `{ "message": "Method not allwoed" }` | Request is not allowed for the resource |

### 5xx: Server Errors
|   Status Code | Body | Usecase |
| --------------| ---------|----------|
| <font color='purple'> **500 Internal Server Error**</font> | `{ "message": "An unexpected error occurred" }`  | Server encountered an unexpected condition  |
| <font color='purple'> **502 Bad Gateway**</font> |  `{ "message": "Invalid response from upstream server" }` | Received an invalid response from the upstream server. |
| <font color='purple'> **504 Gateway Timeout**</font> | `{ "message": "Gateway timeout" }` | Did not receive a timely response from upstream server |