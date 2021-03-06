# Lama  

![lama](lama.png) is a programming language developed by JetBrains Research for educational purposes as an exemplary language to introduce
the domain of programming languages, compilers and tools. Its general characteristics are:

* procedural with first-class functions - functions can be passed as arguments, placed in data structures,
  returned and "constructed" at runtime via closure mechanism;
* with lexical static scoping;
* strict - all arguments of function application are evaluated before function body;
* imperative - variables can be re-assigned, function calls can have side effects;
* untyped - no static type checking is performed;
* with S-expressions and pattern-matching;
* with user-defined infix operators, including those defined in local scopes;
* with automatic memory management (garbage collection).

The name ![lama](lama.png) is an acronym for *Lambda-Algol* since the language has borrowed the syntactic shape of
operators from **Algol-68**; [**Haskell**](www.haskell.org) and [**OCaml**](www.ocaml.org) can be
mentioned as other languages of inspiration.

The main purpose of ![lama](lama.png) is to present a repertoire of constructs with certain runtime behavior and
relevant implementation techniques. The lack of a type system (a vital feature for a real-word language
for software engineering) is an intensional decision which allows to show the unchained diversity
of runtime behaviors, including those which a typical type system is called to prevent. On the other hand
the language can be used in future as a raw substrate to apply various ways of software verification (including
type systems) on.

The current implementation contains a native code compiler for **x86-32**, written
in **OCaml**, a runtime library with garbage-collection support, written in **C**, and a small
standard library, written in ![lama](lama.png) itself. The native code compiler uses **gcc** as a toolchain.

In addition, a source-level reference interpreter is implemented as well as a compiler to a small
stack machine. The stack machine code can in turn be either interpreted on a stack machine interpreter, or
used as an intermediate representation by the native code compiler.

## Language Specification

The language specification can be found [here](lama-spec.pdf).

## Installation

Prerequisites:

* gcc-multilib
* ocaml (>= 4.07.1) [http://ocaml.org]
* opam (>= 2.0.4) [http://opam.ocaml.org]

Installing:

* `opam pin add -n ostap https://github.com/dboulytchev/ostap.git#memoCPS` (remember of "#" being a comment character in bash)
* `opam pin add -y lama https://github.com/JetBrains-Research/Lama.git`

Smoke-testing:

* `pushd tutorial`
* `make`
* `popd`


