# Chapter 5 - The Go CLI Playbook

Source Reference: [The Go CLI Playbook](https://app.pluralsight.com/library/courses/go-cli-playbook/table-of-contents)

## 5.1 Introduction

> The Go Programming language is an open source project to make programmers **more productive.**
> [- Golag](https://golang.org)

The core focus is always on productivity. Go Programming language has these three core characteristics:

1. **Efficient:** Both compiled binaries and code are very efficient.
2. **Clean:** The syntax is very clean, very easy and have very few keywords.
3. **Expansive:** Having more line of code, each one having a more smaller but obvious responsibility is better than having
a more concise language that might take a little longer to learn.
   
## 5.2 The Go Command

The `go` command is the central hub for all the tasks we need to do with Go programs. We can do the below mentioned tasks
with the `go` command.

1. Building applications
2. Testing applications
3. Profiling applications
4. Managing workspaces
5. Interacting with environments

![Go Command Usage](go-command-usage.png)

## 5.3 Building and Running Programs

### 5.3.1 The Run Command

The `go run` command simply runs the go program in memory without building and executable.

```go
$ go help run
usage: go run [build flags] [-exec xprog] package [arguments...]

Run compiles and runs the named main Go package.
Typically the package is specified as a list of .go source files from a single directory,
but it may also be an import path, file system path, or pattern
matching a single known package, as in 'go run .' or 'go run my/cmd'.

By default, 'go run' runs the compiled binary directly: 'a.out arguments...'.
If the -exec flag is given, 'go run' invokes the binary using xprog:
'xprog a.out arguments...'.
If the -exec flag is not given, GOOS or GOARCH is different from the system
default, and a program named go_$GOOS_$GOARCH_exec can be found
on the current search path, 'go run' invokes the binary using that program,
for example 'go_js_wasm_exec a.out arguments...'. This allows execution of
cross-compiled programs when a simulator or other execution method is
available.

The exit status of Run is not the exit status of the compiled binary.

For more about build flags, see 'go help build'.
For more about specifying packages, see 'go help packages'.

See also: go build.
```

```
$ go run src/cmds/hello/hello.go
Hello Go!
```

**Note:** The `GOPATH` environment variable must be set up when running the `go run` command. It is used to find the packages used 
for the program. The `GOROOT` simply specifies the location of the Go binaries.

### 5.3.2 The Build Command

## 5.4 Testing Programs
## 5.5 Managing Workspaces
## 5.6 Interacting with the environment