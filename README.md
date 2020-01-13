# elixir-notes

Lets make a FizzBuzz with no conditional logic.
```elixir
fizz_buzz_logic = fn
  0, 0, _ -> "FizzBuzz"
  0, _, _ -> "Fizz"
  _, 0, _ -> "Buzz"
  _, _, c -> c
end

fizz_buzz_feed = fn
  n -> fizz_buzz_logic.(rem(n, 3), rem(n, 5), rem(n))
end

0..25 |> Enum.to_list |> Enum.map(fn(n) -> fizz_buzz_feed.(n) end)

```
