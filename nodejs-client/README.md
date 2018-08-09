
## 使用方法

```typescript
const c = new Client();

await c.ping();
await c.incr("ns", "key", ms);
await c.get("ns", "key", ms);
```

## 性能测试

```text
Platform info:
- Darwin 17.7.0 x64
- Node.JS: 8.11.3
- V8: 6.2.414.54
  Intel(R) Core(TM) i7-6820HQ CPU @ 2.70GHz × 8


5 tests success:
┌───────────────────────────────┬─────────┬─────────┬─────────┐
│ test                          │ rps     │ ns/op   │ spent   │
├───────────────────────────────┼─────────┼─────────┼─────────┤
│ PING                          │ 55514.0 │ 18013.5 │ 10.008s │
├───────────────────────────────┼─────────┼─────────┼─────────┤
│ INCR (single ns & key)        │ 36618.9 │ 27308.3 │ 10.010s │
├───────────────────────────────┼─────────┼─────────┼─────────┤
│ GET (single ns & key)         │ 40432.5 │ 24732.6 │ 10.004s │
├───────────────────────────────┼─────────┼─────────┼─────────┤
│ INCR (10000 ns & 1000000 key) │ 35722.3 │ 27993.7 │ 10.007s │
├───────────────────────────────┼─────────┼─────────┼─────────┤
│ GET (10000 ns & 1000000 key)  │ 33054.7 │ 30252.9 │ 10.005s │
└───────────────────────────────┴─────────┴─────────┴─────────┘
```