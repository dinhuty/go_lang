Gin Web Framework


Build Status codecov Go Report Card Go Reference Sourcegraph Open Source Helpers Release TODOs

Gin is a web framework written in Go. It features a martini-like API with performance that is up to 40 times faster thanks to httprouter. If you need performance and good productivity, you will love Gin.

Gin's key features are:

Zero allocation router
Speed
Middleware support
Crash-free
JSON validation
Route grouping
Error management
Built-in rendering
Extensible
Getting started
Prerequisites
Gin requires Go version 1.23 or above.

Getting Gin
With Go's module support, go [build|run|test] automatically fetches the necessary dependencies when you add the import in your code:

import "github.com/gin-gonic/gin"
Alternatively, use go get:

go get -u github.com/gin-gonic/gin
Running Gin
A basic example:

package main

import (
  "net/http"

  "github.com/gin-gonic/gin"
)

func main() {
  r := gin.Default()
  r.GET("/ping", func(c *gin.Context) {
    c.JSON(http.StatusOK, gin.H{
      "message": "pong",
    })
  })
  r.Run() // listen and serve on 0.0.0.0:8080 (for windows "localhost:8080")
}
To run the code, use the go run command, like:

go run example.go
Then visit 0.0.0.0:8080/ping in your browser to see the response!

See more examples
Quick Start
Learn and practice with the Gin Quick Start, which includes API examples and builds tag.

Examples
A number of ready-to-run examples demonstrating various use cases of Gin are available in the Gin examples repository.

Documentation
See the API documentation on go.dev.

The documentation is also available on gin-gonic.com in several languages:

English
简体中文
繁體中文
日本語
Español
한국어
Turkish
Persian
Português
Russian
Indonesian
