Q1.9
----

```
(define (+ a b)
  (if (= a 0)
      b
      (inc (+ (dec a) b))))

(define (+ a b)
  (if (= a 0)
      b
      (+ (dec a) (inc b))))
```

最初の手続きのsubstitution model:

```
(+ 4 5)
(inc (+ 3 5))
(inc (inc (+ 2 5)))
(inc (inc (inc (+ 1 5))))
(inc (inc (inc (inc (+ 0 5))))
(inc (inc (inc (inc 5))
(inc (inc (inc 6))
(inc (inc 7))
(inc 8)
9
```

従って，再帰プロセス

二番目:

```
(+ 4 5)
(+ 3 6)
(+ 2 7)
(+ 1 8)
(+ 0 9)
9
```

従って，反復プロセス

Q1.10
-------

```
> (A 1 10)
1024
> (A 2 4)
65536
> (A 3 3)
65536

(define (f n)(A 0 n))
->  2n
(define (g n)(A 1 n))
<s> ->  4*2^(n-2)</s>
-> 2^{n}

(define (h n)(A 2 n))
-> 2^2^...*n times
```



