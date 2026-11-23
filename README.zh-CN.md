# Go 练习题

[English](README.md)

一些独立的 Go 练习，涉及 context、goroutine、channel 和 Redis 加锁。每个示例围绕一个具体行为展开，可以单独阅读。

| 目录 | 示例 |
| --- | --- |
| [test/context_test](test/context_test) | 取消、超时，以及通过 context 传递请求 ID。 |
| [test/goroutine_test](test/goroutine_test) | 有缓冲的 channel、长度和容量。 |
| [test/redis_lock](test/redis_lock) | 加锁练习，包括使用带过期时间的 Redis `SET NX`。 |

## 运行独立练习

[Go 模块](go.mod)声明 Go 1.18。这两个包无需 Redis 即可运行。

```sh
go test ./test/context_test ./test/goroutine_test
```

如需运行 Redis 加锁练习，请使用临时测试实例。该目录也收录了一些独立的 Go 练习。
