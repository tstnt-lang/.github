# 🧩 TSTNT Language

> A modern, lightweight programming language built for speed, simplicity, and fun.  
> Runs on Android (Termux), Linux, and more.

---

## What is TSTNT?

**TSTNT** is a programming language with clean syntax inspired by Rust and Python.  
It comes with a built-in interpreter, package manager, transpiler, LSP, and 100+ packages.

```
use "colors"
use "logger"

struct Player {
    name: str
    hp: int
}

impl Player {
    do greet -> str {
        return "Hello, I am " + self.name
    }
}

do main {
    let p = Player { name: "Alex", hp: 100 }
    print(colors.green(p.greet()))
    logger.info("Player created!")
}
```

---

## 🚀 Quick Start

```bash
# Install (Termux / Linux)
pkg install rust
cargo install --git https://github.com/tstnt-lang/tstnt

# Run a file
tstnt hello.tstnt

# Interactive REPL
tstnt repl

# Install packages
tstnt pkg install logger
tstnt pkg install colors
tstnt pkg search

# Transpile to Python or JS
tstnt transpile hello.tstnt py
tstnt transpile hello.tstnt js

# Watch mode (auto-restart on save)
tstnt watch hello.tstnt

# Run tests
tstnt test tests.tstnt
```

---

## ✨ Language Features

| Feature | Syntax |
|---------|--------|
| Functions | `do greet(name: str) -> str { }` |
| Variables | `let mut x: int = 10` |
| Structs | `struct User { name: str, age: int }` |
| Impl | `impl User { do greet -> str { } }` |
| Match | `match x { 0 -> "zero" _ -> "other" }` |
| Loop | `loop i in 0..10 { }` · `loop x in arr { }` |
| Generics | `do max<T>(a: T, b: T) -> T { }` |
| Optionals | `obj?.field` · `obj?.method()` |
| Ternary | `x > 0 ? "pos" : "neg"` |
| Spread | `let b = [0, ...a, 4]` |
| Try/Catch | `try { throw "err" } catch e { }` |
| Tests | `test addition { assert_eq(1+1, 2) }` |
| Async | `async do fetch { }` · `await expr` |
| Threads | `thread.spawn(|| { })` |
| Pipe | `val \| func \| other` |
| Interp | `"Hello, {name}!"` |
| Enumerate | `loop i, x in arr { }` |
| Imports | `use "./utils.tstnt"` · `use "colors"` |

---

## 📦 Package Manager

```bash
tstnt pkg install <name>     # install
tstnt pkg uninstall <name>   # remove
tstnt pkg list               # installed
tstnt pkg search             # all available
```

Packages live at **[github.com/tstnt-lang/packages](https://github.com/tstnt-lang/packages)** — 100+ packages available.

Popular packages:

| Package | What it does |
|---------|-------------|
| `logger` | Colored logs: info, warn, error, fatal |
| `colors` | Terminal colors |
| `tui` | Terminal UI widgets |
| `stats` | mean, median, std_dev |
| `fake-data` | Generate test names/emails/text |
| `auth` | Register/login/sessions |
| `tg-bot` | Telegram bot helper |
| `tg-rpg` | Full Telegram RPG engine |
| `game-2d` | 2D vectors, collision, ASCII canvas |
| `benchmark-suite` | Benchmark runner with compare |

---

## 🛠 Built-in Modules

`io` `math` `strings` `arr` `json` `time` `env` `fs` `process`  
`crypto` `rand` `fmt` `sys` `path` `buf` `regex` `net`  
`log` `uuid` `term` `bench` `csv` `hash` `thread` `tg`  
`game` `input` `db` `color` `os` `math2` `str2` `num` `type`

---

## 📁 Repositories

| Repo | Description |
|------|-------------|
| [tstnt-lang/tstnt](https://github.com/tstnt-lang/tstnt) | Main compiler/interpreter |
| [tstnt-lang/packages](https://github.com/tstnt-lang/packages) | Official package registry |

---

## 🎯 CLI Reference

```
tstnt <file>                 run file
tstnt repl                   interactive shell
tstnt test <file>            run tests
tstnt build <file>           compile to .tst bytecode
tstnt run <file.tst>         run bytecode
tstnt fmt <file>             format code
tstnt watch <file>           auto-restart on change
tstnt transpile <f> [py|js]  transpile to Python or JS
tstnt pkg install <n>        install package
tstnt pkg search             list all packages
tstnt --version              show version + ASCII art
tstnt --secret               easter egg 🐉
```

---

<div align="center">
  <sub>Built with ❤️ on Android · TSTNT</sub>
</div>
