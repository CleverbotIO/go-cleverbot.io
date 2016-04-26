[![Go Report Card](https://goreportcard.com/badge/github.com/stsy/go-cleverbot.io)](https://goreportcard.com/report/github.com/stsy/go-cleverbot.io)
[![GoDoc](https://godoc.org/github.com/stsy/go-cleverbot.io?status.svg)](https://godoc.org/github.com/stsy/go-cleverbot.io)

# cleverbot.io

[![Join the chat at https://gitter.im/stsy/go-cleverbot.io](https://badges.gitter.im/stsy/go-cleverbot.io.svg)](https://gitter.im/stsy/go-cleverbot.io?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

A Go package for Cleverbot.io.

## Installation
```
go get github.com/stsy/go-cleverbot.io
```

## Usage
```go
// Package main provides a basic example of using go-cleverbot.io.
package main

import (
	"fmt"
	"log"

	"github.com/stsy/go-cleverbot.io"
)

func main() {
	// The api key is given to you at https://cleverbot.io/keys.
	apiUser := "YOUR_API_USER"
	apiKey := "YOUR_API_KEY"

	// apiNick is optional.
	apiNick := ""

	// Initialize Cleverbot
	bot, err := cleverbot.New(apiUser, apiKey, apiNick)
	if err != nil {
		log.Fatal(err)
	}

	// Send Cleverbot a message.
	response, err := bot.Ask("hello world")
	if err != nil {
		log.Fatal(err)
	}

	// Print the response.
	fmt.Println(response)
	// "World? Who is world? My name is Timmy."
}
```
