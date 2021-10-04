## Build Plan
```
[[provides]]
name = "lorem"

[[requires]]
name = "ipsum"

[requires.metadata]
build = true
```

## Caching Reuse Logic
| `lorem` | `ipsum` | `dolor` | Command |
| ------- | ------- | ------- | ------- |
| X | X | X | `sum` |
| X | X | ✓ | `sum` |
| X | ✓ | X | `es` |
| X | ✓ | ✓ | `es` |
| ✓ | X | X | `est` |
| ✓ | X | ✓ | `est` |
| ✓ | ✓ | X | `es` |
| ✓ | ✓ | ✓ | `est` |
