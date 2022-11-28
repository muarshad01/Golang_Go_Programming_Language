# Go-Programming-Language
Learn How To Code: Google's Go (golang) Programming Language [GitHub code link](https://github.com/goestoeleven)

* [Grit - Angela Duckworth](https://www.youtube.com/watch?v=H14bBuluwB8)
* Bill Gates & Warren Buffet -> ONE Attribute for success (_FOCUS_)

***

## Install the latest version of Go
* [Download](https://go.dev/dl/)
* [Go download & Install](https://go.dev/doc/install)

Open the package file you downloaded and follow the prompts to install Go. The package installs the Go distribution to `/usr/local/go`. The package should put the `/usr/local/go/bin` directory in your `PATH` environment variable. You may need to restart any open Terminal sessions for the change to take effect.

Verify that you've installed Go by opening a command prompt and typing the following command:
`$ go version`

Confirm that the command prints the installed version of Go.

```
$ go version
$ go env
$ go help
```

***

## Go workspace
```
<goworkaspace>	# one folder - any name, any location
  |--bin
  |--pkg
  |--src

$ mkdir ~/goworkspace
$ cd ~/goworkspace
$ mkdir bin pkg src

NOTE: Usually, the default go workspace on macOS is $GOPATH=$HOME/go
```

***

## Env variable(s) & PATH setup
```
$ vim ~/.bash_profile

export GOROOT=/usr/local/go
export GOPATH=$HOME/go            # GOPATH needs to point to goworkspace
export GOBIN=$GOPATH/bin
export PATH=$PATH:$GOPATH/bin

$ source ~/.bash_profile
```

***

# Run code
```go
$ go run main.go
$ go run -race main.go
$ go build                # mac: folder-name is executable
$ go install maing.go     # puts the 'executable' in $GOPATH/bin
```

***

## Go Modules: Managing and Updating Dependencies
* [Using Go Modules](https://go.dev/blog/using-go-modules)
* [Tutorial: Create a Go module](https://go.dev/doc/tutorial/create-module#prerequisites)
```go
$ mkdir -p $GOPATH/src/HAPPYDOG
$ cd $GOPATH/src/HAPPYDOG
$ go mod init example/username/repo
$ go mod tidy
$ go test
$ go list -m all

Update

$ go list -m all
$ go get golang.org/x/text
$ go test
$ go get rsc.io/sampler
$ go test
$ go list -m -versions rsc.io/sampler
$ go get rsc.io/sampler@v1.3.1
$ go test
$ go list -m all
```

***
## Using 'go get' to get course code
[cod link](https://github.com/GoesToEleven/GolangTraining)
```go
$ mkdir -p $GOPATH/src/examplegocode
$ cd $GOPATH/src/examplegocode
$ go mod init example.com/test
$ go get -d github.com/GoesToEleven/go-programming/...        # See the '...'
$ cd $GOPATH /pkg/mod/github.com/!goes!to!eleven/!golang!training@v0.0.0-20181204234241-afa19f5c43f3/01_getting-started
```

***

## Useful commands
```go
$ go help
$ go fmt <filename>
$ go fmt ./...          
$ go vet ./...          # reports suspicious structs (code correctness)
$ go lint               # reports poor coding style (style mistakes)
```

***

## Testing & Coverage
* [Package testing](https://pkg.go.dev/testing)
* [Example Code](https://github.com/GoesToEleven/go-programming/tree/master/code_samples/009-testing)
```go
$ go run main.go
$ go test
$ go test -bench .
$ go test -cover
$ go test -coverprofile c.out
$ go tool cover -html=c.out
```
***

## golint
```go
$ mkdir -p $GOPATH/src/test
$ cd $GOPATH/src/test
$ go mod init
$ go get -u golang.org/x/lint/golint
$ go install golang.org/x/lint/golint
$ echo $GOBIN | grep golint
$ golint main.go
```
***

## Documentation
```go
$ go help doc

$ go doc fmt 
$ go doc fmt Print

$ go doc -src fmt 
$ go doc -src fmt Print
$ go doc -src errors New

https://godoc.org/fmt
https://godoc.org/net/http
https://godoc.org/text/template
https://godoc.org/html/template

$ mkdir -p $GOPATH/src/test
$ cd $GOPATH/src/test
$ go mod init
$ go get golang.org/x/tools/cmd/godoc
$ go install golang.org/x/tools/cmd/godoc
$ echo $GOBIN | grep godoc
$ godoc -http=:6060
```

***

## NOTES
```
1. Go is STATIC programming language
2. Everything in Go is "passed by value"
3. There is no "while" or "do-while"
4. Go has "fallthrough" in switch statement
5. "default" case may appear anywhere in a switch statement
6. case can be presented in comma-seperted lists.
7. Everything in Go is PASS BY VALUE (PASS BY COPY or PASS BY REFERENCE throw them away!)
8. There is no try-catch-finally in go
```

***

## Books & Courses
* [Go: The Complete Developer's Guide (Golang) -- Udemy(~9 hrs)](https://www.udemy.com/course/go-the-complete-developers-guide/)
* [The Go Programming Lanauge by Brian W. Kernighan - Book](https://beyondkmp.com/books/golang/The.Go.Programming.Language.pdf) & [code](https://github.com/GoesToEleven/gopl.io)
* [Welcome to Golang Programs](https://www.golangprograms.com/)
* [Go By Example](https://gobyexample.com/)
* [Go Language Specifiction](https://go.dev/ref/spec)
* [Effective Go](https://go.dev/doc/effective_go)
* [An Introduction to Progrmming in Go by Caleb Doxey](https://www.golang-book.com/public/pdf/gobook.pdf)
* [Pro Go: The Complete Guide to Programming Reliable and Efficient Software Using Golang 1st ed. Edition](https://www.amazon.com/Pro-Go-Complete-Programming-Efficient/dp/1484273540)
* [Practical Go: Building Scalable Network and Non-Network Applications 1st Edition](https://amsaha.bitbucket.io/)
* [Efficient Go - 2022](https://www.oreilly.com/library/view/efficient-go/9781098105709/)
* [Go in Action](https://www.manning.com/books/go-in-action)
* [How to Write a Book: Introduction](https://www.doxsey.net/blog/how-to-write-a-book--introduction/)
* [Mastering Go: Harness the power of Go to build professional utilities and concurrent servers and services, 3rd Edition 3rd ed. Edition]()
* [Learning Go: An Idiomatic Approach to Real-World Go Programming 1st Edition]() 

### Concurrency
* [Concurrency in Go; Tools and Techniques for Developers by Katherine Cox-Buday (O’Reilly 2017)](https://www.amazon.com/Concurrency-Go-Tools-Techniques-Developers/dp/1491941197)

### Design patterns
* [Design Patterns](https://golangbyexample.com/all-design-patterns-golang/)
* [Go Language Patterns](http://www.golangpatterns.info/)
* [All Design Patterns in Go (Golang)](https://golangbyexample.com/all-design-patterns-golang/)
* [GoF Design patterns that still make sense in Go](https://dev.to/mauriciolinhares/gof-design-patterns-that-still-make-sense-in-go-27k5)

### Testing
* [Learn Go with tests](https://quii.gitbook.io/learn-go-with-tests/)

### Web Programming
* [Learn Web Programming in Go by Examples](https://gowebexamples.com/)

***

## Tools
* [JSON-to-Go Convert](https://mholt.github.io/json-to-go/)
* [Go online Playground](https://play.golang.org/)
* [Better Go Playground](https://goplay.tools/)

***

## Useful Articles
* [Error handling and Go](https://go.dev/blog/error-handling-and-go)
* [Defer, Panic, and Recover](https://go.dev/blog/defer-panic-and-recover)
* [Frequently Asked Questions (FAQ)](https://go.dev/doc/faq#exceptions)
* [Go Forum](https://forum.golangbridge.org/)
* [Go Blog](https://go.dev/blog/)
* [Using Go Modules](https://go.dev/blog/using-go-modules)
* [JSON and Go](https://go.dev/blog/json)
* [Go Proverbs](https://go-proverbs.github.io/)
