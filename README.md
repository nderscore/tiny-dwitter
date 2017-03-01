# Tiny Dwitter

A tweet-sized clone of [lionleaf](https://github.com/lionleaf)'s [dwitter](https://www.dwitter.net) in 139 bytes.

```html
<body onload="setInterval('t=new Date/1e3;R=(...z)=>`rgba(`+z;x=c.getContext`2d`;with(Math)eval($.value)',16)"><input id=$><p><canvas id=c>
```

### Try it out [here](http://cdn.rawgit.com/nderscore/tiny-dwitter/32d760c4/index.html)!

### Instructions

* Your function is called every ~16 ms (roughly 60-ish times per second).
* `t` - Current timestamp in seconds.
* `sin` - Shorthand for `Math.sin`.
* `cos` - Shorthand for `Math.cos`.
* `tan` - Shorthand for `Math.tan`.
* `R` - Function that generates rgba-strings, usage ex.: `R(255, 255, 255, 0.5)`
* `c` - A 300x150 canvas.
* `x` - A 2D context for that canvas. 

### Compromises/Differences From Dwitter

 * The canvas is the default size of 300 x 150 instead of 1920 x 1080.
 * `requestAnimationFrame` is not used, instead an approximation of 60-ish fps is achieved with a 16ms interval.
 * `t` variable is not a seconds counter starting from 0. Instead, it is the current timestamp in seconds.
 * Trig method shortcuts are `sin` `cos` and `tan` instead of `S` `C` and `T`.  *Bonus: All `Math` methods are available too!*
 * Arguments passed to `R` are not optional and are not automatically converted to numbers.
 * 140 character limitation is not implemented (*I had to scrap it to include the `R()` function and stay under 140 bytes* 😞)

### Greetz

* Special thanks to [p01](http://www.p01.org) for being my golf caddy on this.
