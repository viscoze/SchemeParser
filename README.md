# Scheme Parser

#### To run the REPL:
```
cd chapter10-standard-library
runhaskell SchemeParser.hs
```
Once in the REPL, you can load the standard library file, and run some code.
```
Lisp>>> (load "stdlib.scm")
(lambda ("pred" "lst") ...)
Lisp>>> (map (curry + 2) '(1 2 3 4))
(3 4 5 6)
Lisp>>> (filter even? '(1 2 3 4))
(2 4)
```  
#### Or, to run a file:
```
runhaskell SchemeParser.hs <inputfile>
```


## Basic syntax

Console output
```
(display "abc")
```

Variable bound to a number:
```
(define f 10)
```

Condition
```
(if (> 2 3)
  (print "2")
  (print "3"))
```

Loop
```
(let loop ((i n) (res '()))
    (if (< i 0)
        res
        (loop (- i 1) (cons (* i i) res)))))
```

## Strings

```
(substring "abcdefg" 2 3)

(string-append "abc" "xyz")
```
