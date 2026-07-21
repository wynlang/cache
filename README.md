# cache - Official Wyn Package

In-memory key-value cache. Pure Wyn (wraps HashMap).

## Install

```bash
wyn pkg install github.com/wynlang/cache
```

## Usage

```wyn
var cache = HashMap.new()
cache.insert("user:1", "Alice")
var user = cache.get("user:1")  // "Alice"
```
