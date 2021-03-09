# Pop

This is a coding exercise to test your understanding of Elixir and OTP.

## To get the Phoenix server started

- Install dependencies with `mix deps.get`
- Start Phoenix endpoint with `mix phx.server` or `iex -S mix phx.server`.

## Challenge part.

1. Build an endpoint that can accept Fahrenheit, Celsius or Kelvin temperatures and returns the Fahrenheit, Celsius and Kelvin conversions of that temperature. So, if the request is something like `{"degrees": 70.5, "type": "celsius"}` then the response should be something like `{"celsius": 70.5, "fahrenheit": 158.9, "kelvin": 343.65}`. This endpoint should accept all valid temperatures, and return an error message when the conversion cannot be done.
2. Make the endpoint stateful. You should memoize the response. So, if someone requests the conversion of 70.5 degrees Celsius twice, then the first request calculates the conversion and caches it. The second request doesn't get a calculated response, but instead the response just contains the cached values. We're looking for a solution that uses GenServer or some other similar OTP construct. ETS, Postgresql, Redis, or other database focused solutions are not acceptable for this part. There is a controller template at `lib/pop_web/controllers/temperature_controller.ex`. There is also a testing template at `test/pop_web/controllers/temperature_controller_test.exs`.

## Tests

- Elixir tests will be run with `mix test`

Once you've started the server with `mix phx.server` then you can visit [`localhost:4000`](http://localhost:4000) from your browser.

## Learn more

- Official website: https://www.phoenixframework.org/
- Guides: https://hexdocs.pm/phoenix/overview.html
- Docs: https://hexdocs.pm/phoenix
- Forum: https://elixirforum.com/c/phoenix-forum
- Source: https://github.com/phoenixframework/phoenix
