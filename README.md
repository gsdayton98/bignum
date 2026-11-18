# BigNumber

My implementation of an extended precision library.

Intent is to be as simple as possible but no simpler. Functions that can
generate an error return a std::optional<> instead. Constructors are private,
and only perform structure like initialization. Constructions that can produce
an error use a generator function that returns a std::optional<> instead.

## Errors
Functions return an optional rather than some error type to keep the interface
as simple as possible but no simpler. I could return an error that
contains varying amounts of information according to the type of error, but the
huge disadvantage of such interfaces is they become projects in themselves. One
change in the error framework triggers everything to be rebuilt. I'm relying on
the function getting called that returns the error is enough of a clue of what
went wrong.


