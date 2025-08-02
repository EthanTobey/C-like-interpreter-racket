# C-like Interpreter in Racket

A functional interpreter for a simplified object-oriented language, written in Racket. The interpreter supports both functional and object-oriented constructs, including class definitions, field access, method invocation, and stateful object behavior.

---

## 📌 Overview

This project implements an interpreter for a C-like language using Racket, showcasing concepts such as recursive evaluation, scoped environments, and simulated object-oriented features in a functional programming language.

The main functionality is defined in `Interpreter.rkt`, which provides an `interpret` function to evaluate source files containing code written in the target language.

---

## 🧠 Core Functionality

### Main Entry Point

```racket
(interpret "filename")
```

---

## File Structure

C-like-interpreter-racket/
│
├── Interpreter.rkt          # Main interpreter logic and evaluation functions
├── classParser.rkt          # Parses source code into ASTs
├── simpleParser.rkt         # Handles lower-level parsing tasks
├── lex.rkt                  # Lexical analysis functions
│
├── Test1.rkt                # Runs functional code test suite
├── Test2.rkt                # Runs object-oriented test suite
│
├── tests1/
│   └── test(0-20).txt            # Input test cases for functional code
├── tests2/
│   └── test(0-7).txt             # Input test cases for OOP code
│
├── README.md
└── LICENSE (optional)

---

### Naming Convention

Within `Interpreter.rkt`, function prefixes indicate what kind of data the function returns:

- `S_` → Returns a modified **state**
- `V_` → Returns a **value**
- `SV_` → Returns both a **state and a value**

This naming system distinguishes between pure evaluators, environment transformers, and state-aware operations.

---

## 🚀 How to Run

### Requirements

- Install Racket: [https://racket-lang.org](https://racket-lang.org)

### Run Predefined Tests

You can run either the functional or object-oriented test suite:

```bash
# Run functional test suite
racket Test1.rkt

# Run object-oriented test suite
racket Test2.rkt
```

---

### Run a Custom Test

Edit the input file at `tests1/test.txt` (for functional tests) or `tests2/test.txt` (for object-oriented tests).

Then run the appropriate test file:

```bash
racket Test1.rkt    ; to run custom functional test
racket Test2.rkt    ; to run custom object-oriented test
```

---

### Manual Interpreter Use

You can also run the interpreter directly from any Racket file or the REPL:

```racket
(require "Interpreter.rkt")
(interpret "yourfile.txt")
```

---

## 🧪 Language Features

- Class definitions with fields and methods  
- Object instantiation and field access  
- Variable declaration and shadowing  
- Arithmetic and conditional expressions  
- Method invocation and return values  
- Stateful object behavior (mutating fields)  
- Separate functional and object-oriented evaluation logic  

---

## 📎 Notes

- `classParser.rkt` handles top-level parsing of the custom language syntax.  
- `simpleParser.rkt` and `lex.rkt` support lexical and expression parsing.  
- `Test1.rkt` and `Test2.rkt` demonstrate two distinct paradigms: **functional** and **object-oriented**.  
- Input programs are plain text, parsed into ASTs, and interpreted via recursive evaluation.  

---

## 🧑‍💻 Author

**Ethan Tobey** — [GitHub](https://github.com/yourusername)  
Case Western Reserve University  
B.S. in Computer Science, Minor in Computer Gaming  
