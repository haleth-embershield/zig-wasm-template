# zig-wasm-template
A simple template for building and serving WebAssembly (WASM) applications using Zig.

## Features
- Compatible with Zig v0.13
- Simple template for building and serving WASM applications
- Includes setup for http-zerver (see `setup_zerver.zig`)
- Works on Windows and Linux (macOS untested)
- Fake favicon.ico and robots.txt

## Usage
This template provides a straightforward way to build Zig code targeting WebAssembly and serve it locally.

### Server Options
- The included `setup_zerver.zig` will set up http-zerver for serving your WASM files
- Alternatively, you can use other simple HTTP servers like:
  ```
  python -m http.server
  ```
  or
  ```
  npx serve
  ```

## Getting Started
1. Clone this repository
2. Use one of the following build commands:

   - **Build, deploy, and start the server in one step:**
     ```
     zig build run
     ```
     This command will:
     - Compile your Zig code to WebAssembly
     - Copy the WASM file and assets to the www directory
     - Start http-zerver on port 8000
     - Access your application at http://localhost:8000

   - **Build and deploy without starting the server:**
     ```
     zig build deploy
     ```
     This command will:
     - Compile your Zig code to WebAssembly
     - Copy the WASM file and assets to the www directory
     - You can then use your preferred HTTP server to serve the www directory

   - **Just build the WASM file:**
     ```
     zig build
     ```
     This will compile your code to WASM without copying files or starting a server
