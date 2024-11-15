# Rust🦀 with WASM🛠️!

This is just a simple project which uses a Rust function which is called through JavaScript! Made possible by the incredible WASM support!!!

## Explaination

1. **_Rust program_**: 
We first write a function in the `/src/lib.rs` file. Using the wasm library for rust, we declare the `greet` function as a function which is to be exported and used in JavaScript.

2. **_The Wrapper_**:
Then we build the rust program. Sequently we also build the wrapper for the rust program to be used in JavaScript.

3. **_Usage_**: 
We use the functions of the rust program in our JavaScript in `index.html` file through the wrapper we just made. 

4. **_Output_**: 
The website created just says 2 lines, the first one is "WebAssembly with Rust" which is a h1 tag hardcoded into the html file, which the other sentence is the output from the Rust program! 

So basically we just integrated Rust programs in JavaScript through WASM!

## Steps to get it working

Add a web-assembly target in your local rust compiler
```
rustup target add wasm32-unknown-unknown
```

Install the web assembly target
```
rustup target add wasm32-unknown-unknown
```

Build for the web assembly target 
```
cargo build --target wasm32-unknown-unknown --release
```

Install the WASM tool which builds the wrapper
```
cargo install wasm-pack
```

Build the JavaScript wrapper
```
wasm-pack build --target web
```

Run the http server using NPX
```
npx run test
```