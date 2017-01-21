# Coding in Go when you come from Erlang world

One or  two year ago,  I had  tried Go. After  one day, I  switched to
another language. Sorry Go, if I want to write something similar to C,
I  write C  code! After  doing that,  I've tried  lot of  language, on
different paradigm, Haskell, Erlang, Elixir, Rust, OCaml... Erlang was
clearly a good choice. So? Why try Go today?

## Starting Go

This week, one friend of mine tell me: «Go is pretty awesome! Just try
it!». So,  you now  what? I will  try to learn  Go with  Erlang. Seems
pretty interesting! So, first, to  make something working from scratch
in erlang, I will use escript.

```erlang
#!/usr/bin/env escript
%% -*- erlang -*-
%%! -smp enable

main(_) ->
  hello("world").

hello(X) ->
  io:format("hello ~p~n", [X]).
```

Similar code in Go:

```go
package main

import "fmt"

func main() {
  hello("world")
}

func hello(x string) {
  fmt.Println("hello " + x)
}

```

To run Erlang and Go code:

```sh
escript hello.escript
go run hello.go
```
