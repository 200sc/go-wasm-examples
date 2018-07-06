# go-wasm-examples
Some small examples of using Go and WebAssembly

# Usage

The `server` directory contains a very small HTTP server implementation that simply hosts the files of the current working directory.
It also downloads the `wasm_exec.js` JavaScript bridge from the official golang repository, if the file doesn't already exist.

```bash
go build ./server
./server
```


## Example 1:

The first example prints a "Hello World" to the console of the browser.
Browse to http://localhost:3000 after building the example:

```bash
go build -o test.wasm ./wasm1
```

## Example 2:

The second example interacts with the DOM of the page and enables the "Stop" button.
It also registers a click handler on the button and keeps the go program alive until the button was pressed.
Browse to http://localhost:3000 after building the example:

```bash
go build -o test.wasm ./wasm2
```