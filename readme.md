1. [ ] type-system
2. [ ] tasks
3. [ ] states
3. [ ] apis
4. [ ] dashboards


# type system

no ideas

# tasks


# design goals:

1. native on kubernetes (scale, failure recovery)
2. as a library, not a service like flink (host many job)
3. wasm based api extension
4. no zookeeper, no yarn, no any specified componments, all dependencies should be alternativily.

<pre>
                     mini-batch (library)
                           |
                           |
                           |
                           ↓
user-code → dag with udf → + → assembly → executable
</pre>

## refs

scotch - 为Rust程序实现Wasm插件系统
scotch 能实现与wasm插件复杂类型的交互，目标是实现为任何Rust程序方便引入wasm插件系统实现框架。

[scotch](https://github.com/ItsEthra/scotch)

Rust的通用Wasm plugin解决方案
写得太好了，直接阅读原文吧。

[plugin for rust](https://reorchestrate.com/posts/plugins-for-rust/)

使用 quickjs-wasm-rs 和 wasmtime 为Rust程序实现一个安全的隔离的插件系统。

[quickjs-wasm-rs](https://github.com/seddonm1/quickjs)


# start point:

1. read from socket
2. imply groupBy or keyBy
3. sum
4. and then another groupBy
5. window
6. sink to stdout
