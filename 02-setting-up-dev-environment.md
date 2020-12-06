## Setting up a Dev Environment

- https://golang.org
- `GOROOT` needs to be set if you're installing a tarball binary and not using
  the instructed location
- Set `GOPAtH` to `$HOME/golib`
- Also add `$GOPATH/bin` to the `PATH` env var
- First segment of GOPATH is used when we `go get`
- All segments are searched for libraries in our go code
- Set `GOPATH=$HOME/golib:$HOME/projects/golang-learn`
- `pkg` folder has intermediary compile stuff
- `src` folder

### Environment variables

1. `GOPATH` can and should have multiple paths.
  - The first path is special and it is where libraries are placed on `go get`. Set
    to `$HOME/golib`
  - Other paths are searched for libaries. Choose a go project path, e.g. `$HOME/projects/gocode`
2. `PATH` add all the `GOPATH` `bin`s so you can run your binaries
3. `GOROOT` avoid setting this

### Folder structure

- You'll want your foler structure to have three folders:
  - `bin`
  - `pkg`
  - `src`

- Each project in `src` folder should emulate your github project path for its path

### Creating first app

At `src/github.com/username/appname/Main.go`

```go
package main

import "fmt"

func main() {
  fmt.Println("Hello world")
}
```

To run:

```shell
go run src/github.com/username/appname/Main.go
```

to build:

```shell
go build github.com/username/appname
```

to install:

```shell
go install github.com/username/appname
```

### Package locations

Everything in your `GOPATH` and `/usr/local/go/src`