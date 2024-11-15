# Rust🦀 with WASM🛠️!

This is just a simple project which uses a Rust function which is called through JavaScript! Made possible by the incredible WASM support!!!

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