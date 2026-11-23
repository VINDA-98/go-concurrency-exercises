# Go Practice Exercises

[简体中文](README.zh-CN.md)

Small Go exercises for experimenting with contexts, goroutines, channels and Redis locking. Each example focuses on one behavior that can be read in isolation.

| Directory | Examples |
| --- | --- |
| [test/context_test](test/context_test) | Cancellation, timeouts and passing a request ID through a context. |
| [test/goroutine_test](test/goroutine_test) | Buffered channels, length and capacity. |
| [test/redis_lock](test/redis_lock) | Locking exercises, including a Redis `SET NX` example with a key expiry. |

## Run the standalone exercises

The [Go module](go.mod) declares Go 1.18. These two packages can run without a Redis instance.

```sh
go test ./test/context_test ./test/goroutine_test
```

Use a disposable Redis instance if you try the Redis lock exercise. That package also contains standalone Go experiments.
