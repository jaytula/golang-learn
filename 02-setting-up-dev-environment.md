## Setting up a Dev Environment

- https://golang.org
- `GOROOT` needs to be set if you're installing a tarball binary and not using
  the instructed location
- Set `GOPAtH` to `$HOME/golib`
- Also add `$GOPATH/bin` to the `PATH` env var
- First segment of GOPATH is used when we `go get`
- All segments are searched for libraries in our go code
- Set `GOPATH=$HOME/golib:$HOME/code`
- `pkg` folder has intermediary compile stuff