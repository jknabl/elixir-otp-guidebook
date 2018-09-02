# Chapter 1: Introduction

* Built on Erlang VM
* Erlang: built to handle soft realtime, distributed, and concurrent systems
  * Built for Ericsson's telephone switches
  * VM scheduler automatically distributes workloads across processors

* Functional programming language.
  * Immutable state
  * High-order functions
  * Lazy evaluation
  * Pattern matching
* Metaprogrammable. Code can be represented as data and vice-versa.
* OTP (Open Telecom Platform)

## Tooling

* `iex` : interactive elixir. REPL similar to `irb` in Ruby.
  * Allows connecting to 'nodes' from the shell
  * `IEx.pry`, to inspect environment in real time, like `binding.pry` in Ruby.
* ExUnit test framework. 
* `mix` build tool for compiling and testing Elixir projects
  * Like `rake` in Ruby or `lein` in Clojure
* Standard library is relatively complete. Has cool stuff like `Stream` which lets you build composable, lazy enumerables. 
* Metaprogramming with macros.

* Can use pretty much any Erlang library with Elixir.
* Phoenix. Web framework similar to Rails.

* Good for soft realtime systems.
  * Soft realtime: can miss some deadlines/promises, but too many missed degrades performance.
  * Hard realtime: any missed deadline/promise is a system failure.

* One of the critical features of OTP is **behaviours**. 
  * For a behaviour, OTP expects you to fill in certain functions. When you do, OTP takes care of async or sync message handling, concurrency errors (deadlocks/race conditions), fault tolerance, and failure handling.
    * `GenServer` and `Supervisor` are two of the most-used behaviours. 

* Contains a thing called `Dialyzer` that handles some of the stuff a static type system would normally take care of. 