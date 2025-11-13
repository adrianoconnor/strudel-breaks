These are all normalized to two bars long and -12b volume

https://www.youtube.com/watch?v=dcmwqqzJubA

```
setGainCurve(x => Math.pow(x, 2))
samples('github:switchangel/breaks')
samples('github:switchangel/pad')
samples('github:tidalcycles/uzu-drumkit')
setCps(150/60/4)

$: s("breaks/2").n(4).gain(0.9).fit()
  .scrub(
    irand(16)
    .div(16)
    .segment(8)
    .ribbon("<10 20>", 1)
    .almostNever(ply("2 | 4"))
  )
```
