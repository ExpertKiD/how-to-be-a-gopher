# Chapter 1 - Introduction

Go is a general-purpose language designed with systems programming in mind. It is strongly typed and garbage-collected and has explicit support for concurrent programming. Programs are constructed from packages, whose properties allow efficient management of dependencies.

The grammar is compact and simple to parse, allowing for easy analysis by automatic tools such as integrated development environments.

##1.1 The Program

Let's now start writing our very first program. It is as you can guess a simple Hello World program.

**File: hello.go**
```go
package main

import (
    "fmt"
)

func main() {
    fmt.Println("Hello, World!")
}
```

First, all go program need a `main` package to run the program. Inside the main package, one file must contain the entry point to the application. The entry point is the `main()` function. Second, all the imports used in the go file must be listed.

**Note:** Go program must use all the imports. Otherwise, an error will be thrown while running the program stating to either use the import or remove it.

## 1.2 Go Comments
Comments are useful for documentation in a Go file and are ignored by the compiler. There are two types of comments:

* a single-lined comment is preceded by a double forward slash, `//`, and ends at the end of the line.
* a multi-lined comment begins with `/*` followed by one or more lines of comments and ends with `*/`

```go
// one line comment

/*
this comment
is on multiple lines
and ends here
*/
```
## 1.3 Go Documentation
In Go, comments can be used as built-in documentation. To check the role of a function, in the command line, use the 
command `go doc` followed by a package or the function of a package. For example:

```go
$ go doc fmt
To find more information about a package’s function:

$ go doc fmt.println
Import Multiple Packages
```

To import multiple packages in a Go file, use the `import` keyword followed by the package name enclosed in double-quotes
and repeat this statement for every imported package on its own line, or write a single import keyword to import multiple
packages, one per line, in enclosed parentheses, (…).

```go
import "fmt"
import "math"
import "time"
```
or

```go
import (
"fmt"
"math"
"time"
)
```

## 1.4 Go Compiler
As a compiled language, Go does not run until its source file is processed through a separate software called a compiler
to produce a final executable program. The Go compiler can be accessed on the command line via a generic command such as:

```go
go <command> [arguments]
```

## 1.5 Packages in Go
A Go package is a directory made up of a collection of Go source files that are compiled together. This collection of 
reusable code typically contains functions related to a specific topic or concept. To use code from a particular package,
we simply import it into our Go source file.

For example, to import the fmt package which contains functions for formatting input and output strings, we type the 
keyword import followed by the package name.

```go
import "fmt"
```

# 1.6 Running Files in Go
The Go compiler can execute Go code from the source file without producing an executable file. Instead of build, use run. To do this, type the following in the command line:

```go 
$ go run exampleFile.go
```

# 1.7 Compile Go
The Go compiler takes a Go source file with a .go extension, processes it and produces an executable file without any extension. To compile a Go source file, test.go, type at the command line:

```go
$ go build test.go
```

This will produce an executable file, test. To run test, type in the command line:

```go 
$ ./test
```

Go Import Package
To import a single package in a Go file, use the keyword import followed by the package name in double-quotes.
