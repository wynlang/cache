# cache - Official Wyn Package

In-memory key/value cache. Pure Wyn.

## Install

```bash
wyn pkg install github.com/wynlang/cache
```

## Usage

The cache is a single string value you hold and pass back in; mutating
operations return the updated store. (A Wyn `HashMap` cannot cross a module
import boundary, so the importable surface is string-serialized.)

```wyn
import cache

var c = cache.cache_new()
c = cache.cache_set(c, "user:1", "Alice")
var user = cache.cache_get(c, "user:1")   // "Alice"
c = cache.cache_delete(c, "user:1")
```

Public API:

- `cache_new() -> string`
- `cache_set(store, key, value) -> string` (returns the updated store)
- `cache_get(store, key) -> string` (`""` if absent)
- `cache_has(store, key) -> bool`
- `cache_delete(store, key) -> string`
- `cache_size(store) -> int`
