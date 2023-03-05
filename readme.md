
- [ ] type-system
- [ ] tasks
- [ ] states
- [ ] apis
- [ ] dashboards


## type system

no ideas

## tasks

no plans

## design goals:

1. native on kubernetes (scale, failure recovery)
2. as a library, not a service like flink (which host many jobs)
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

### refs

+ **scotch** - wasm plugin system for Rust

scotch provides complex interactivity between wasm plugin systems and rust, in order to help any rust projects enhanced with wasm plugin systems.

[scotch](https://github.com/ItsEthra/scotch)

+ a general wasm plugin draft for rust project

[plugin for rust](https://reorchestrate.com/posts/plugins-for-rust/)

+ build a plugin system for rust project with safety and isolated env using `quickjs-wasm-rs` and `wasmtime`

[quickjs-wasm-rs](https://github.com/seddonm1/quickjs), [wasmtime](https://github.com/bytecodealliance/wasmtime)


# start point:

1. read from socket
2. imply groupBy or keyBy
3. sum
4. and then another groupBy
5. window
6. sink to stdout
