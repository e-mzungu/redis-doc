@complexity

O(log(N)+M) with N being the number of elements in the
sorted set and M the number of elements returned.

Returns the specified range of elements in the sorted set stored at `key`. The
elements are considered to be ordered from the highest to the lowest score.

Apart from the reversed ordering, `ZREVRANGE` is similar to `ZRANGE`.

@return

@multi-bulk-reply: list of elements in the specified range (optionally with
their scores).

@examples

    @cli
    ZADD myzset 1 "one"
    ZADD myzset 2 "two"
    ZADD myzset 3 "three"
    ZREVRANGE myzset 0 -1
    ZREVRANGE myzset 2 3
    ZREVRANGE myzset -2 -1

