# Project README

## Overview
- The project is a C program that uses neural networks to recognize digits from images. It includes training and testing phases.

## Features
- Neural network for image recognition
- Training of the neural network on digit images
- Testing the trained neural network on test images
- Use of static libraries for graphics and neural network functionality

## Project Structure
- `build/` - Compiled binary files produced by Main.c
- `src/` - Source code directory containing Main.c and header files
  - `Main.c` - Entry point of the program
  - Header files - Standalone header-based C-files without accompanying implementation files

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed for graphics and neural network functionality:
  - Graphics: GSprite.h
  - Neural Network: NeuralNetwork.h

## Build & Run
- **Linux**:
  ```sh
  cd /home/codeleaded/Hecke/C/Cmd_ImgCfy_AI
  make -f Makefile.linux all
  ```
  To run the executable:
  ```sh
  ./build/Main
  ```

- **Windows**:
  ```sh
  cd C:\path\to\Cmd_ImgCfy_AI
  make -f Makefile.windows all
  ```
  To run the executable:
  ```sh
  build\Main.exe
  ```

- **Wine (Linux Cross Compile for Windows)**:
  ```sh
  cd /home/codeleaded/Hecke/C/Cmd_ImgCfy_AI
  make -f Makefile.wine all
  ```
  To run the executable within Wine:
  ```sh
  WINEPREFIX=~/wine64 WINEARCH=win64 wine build/Main.exe
  ```

- **Web (Emscripten)**:
  ```sh
  cd /home/codeleaded/Hecke/C/Cmd_ImgCfy_AI
  make -f Makefile.web all
  ```
  To run the WebAssembly file using wasmtime:
  ```sh
  wasmtime build/Main.wasm
  ```

- **Build Options**:
  - `make -f Makefile.(os) all` - Build output
  - `make -f Makefile.(os) do` - Build + executable output
  - `make -f Makefile.(os) clean` - Remove build artifacts