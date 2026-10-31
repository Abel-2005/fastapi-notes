2. API (Application Programming Interface)

An API is a set of defined rules, protocols, and mechanisms that allows two or more software applications or components to communicate, exchange data, and interact with each other.

3. FastAPI

FastAPI is a modern, high-performance Python web framework used for building APIs.

It is built on top of two important Python libraries:

Starlette: Handles the web-related functionality, including routing, request handling, and responses.

Pydantic: Handles data validation and serialization, ensuring that incoming and outgoing data follows the expected structure and format.

4. Starlette

Starlette is a lightweight ASGI framework/toolkit used by FastAPI to handle web-related functionality.

It manages:

Receiving HTTP requests.

Routing requests to the appropriate endpoints.

Sending HTTP responses.

Middleware and WebSocket functionality.

5. Pydantic

Pydantic is a Python data validation library used by FastAPI to validate, parse, and serialize data.

It checks whether the data coming into an API:

Has the correct data types.

Follows the expected structure.

Meets the defined validation rules.

If the incoming data is invalid, FastAPI automatically generates an appropriate validation error response.


## 6. Advantages of FastAPI

1. **Fast Development:** Increases development speed with less boilerplate code.
2. **Automatic Input Validation:** Uses Pydantic to automatically validate incoming data.
3. **Auto-generated Interactive Documentation:** Generates API documentation using OpenAPI and Swagger UI.
4. **Asynchronous Programming Support:** Supports asynchronous programming using `async` and `await`.
5. **High Performance:** Provides high performance due to Starlette and its ASGI-based architecture.
6. **Type Hints:** Uses Python type hints to improve code readability, validation, and editor support.

## 7. FastAPI Request-Response Architecture

The basic flow of an HTTP request in FastAPI is:

```text
Client / Browser
       |
       | HTTP Request
       v
ASGI Server (Uvicorn)
       |
       | ASGI Interface
       v
Python Web Application
       |
       v
FastAPI
       |
       v
Endpoint / Business Logic
       |
       v
HTTP Response
       |
       v
Client / Browser
```

### 8. WSGI (Web Server Gateway Interface)

- WSGI stands for Web Server Gateway Interface.
- It is a standard interface for connecting Python web applications with web servers.
- It was traditionally designed for synchronous request-response handling.
- It is commonly used by traditional Python web frameworks such as Flask and traditional Django deployments.

### 9. ASGI (Asynchronous Server Gateway Interface)

- ASGI stands for Asynchronous Server Gateway Interface.
- It is the modern successor to WSGI.
- It supports asynchronous applications.
- It supports HTTP, WebSockets, and other asynchronous communication protocols.
- It can handle both synchronous and asynchronous application code.

### 10. Difference Between WSGI and ASGI

| Feature           | WSGI                         | ASGI                                  |
| ----------------- | ---------------------------- | ------------------------------------- |
| Full form         | Web Server Gateway Interface | Asynchronous Server Gateway Interface |
| Programming model | Primarily synchronous        | Synchronous and asynchronous          |
| WebSockets        | Not natively supported       | Supported                             |
| HTTP handling     | Supported                    | Supported                             |
| Async support     | No native async support      | Native async support                  |
| Common server     | Gunicorn                     | Uvicorn                               |

**Important:** FastAPI is an ASGI-based framework. Uvicorn is a commonly used ASGI server for running FastAPI applications.
