# Упражнение 1
```hs
MacBook-Air-Nikita:~ n1kutochkin$ ghci
GHCi, version 8.10.7: https://www.haskell.org/ghc/  :? for help
Prelude> shortFunc x = (3.14 * (x*x)

<interactive>:1:28: error:
    parse error (possibly incorrect indentation or mismatched brackets)
Prelude> shortFunc x = (3.14 * (x*x))
Prelude> lambdaFunc = \x -> (3.14 * (x*x))
Prelude> shortFunc 5
78.5
Prelude> lambdaFunc 5
78.5
```
# Упражнение 2
1. `area x = 3.14 * (x * x)`
2. `double x = x * 2`
3. 
```haskell
let x = 7
    y = 10
in x + y    
```

# Упражнение 3
###  `let x = 5 in x`
Ответ: 5

GHCI: 
```hs
Prelude> func = let x = 5 in x
Prelude> func
5
```

### `let x = 5 in x * x`
Ответ: 25

GHCI:
```hs
Prelude> func = let x = 5 in x * x
Prelude> func
25
```
### `let x = 5; y = 6 in x * y`
Ответ: 30

GHCI:
```hs
Prelude> func = let x = 5; y = 6 in x * y
Prelude> func
30
```

### `let x = 5; y = 1000 in x + 3`
Ответ: 8

GHCI:
```hs
Prelude> func = let x = 5; y = 1000 in x + 3
Prelude> func
8
```
### `let y = 10; x = 10*5 + y in x * 5`
Ответ: 300

GHCI:
```hs
Prelude> func = let y = 10; x = 10*5 + y in x * 5
Prelude> func
300
```
### 
```haskell
let x = 7
    y = negate x
    z = y * 10
in z / x + y    
```
Ответ: -17

GHCI:
```haskell
Prelude> :{
Prelude| func = let x = 7
Prelude|            y = negate x
Prelude|            z = y * 10
Prelude|        in z / x + y
Prelude| :}
Prelude> func
-17.0
```
# Упражнение 4
2. `let x = 5 in x * x`
```haskell
first = x * x
  where x = 5
```
3. `let x = 5; y = 6 in x * y`
```hs
snd = x * y
  where
    x = 5
    y = 6
```
4. `let x = 5; y = 1000 in x + 3`
```hs
trd = x + 3
  where
    x = 5
    y = 1000
```
5. `let y = 10; x = 10*5 + y in x * 5`
```hs
fourth = x * 5
  where
    y = 10
    x = 10 * 5 + y
```
6. 
```hs
fifth = z / x + y
  where
    x = 7
    y = negate x
    z = y * 10
```

# Упражнение 5
```hs
Prelude> x = 10
Prelude> 7 + x
17
Prelude> (+7) x
17
Prelude> (-) 7 x
-3
Prelude> (-) x 7
3
Prelude> (subtract 5) x
5
Prelude> (-x) + x
0
```

# Упражнение 6
```hs
Prelude> myAbs x = if x < 0 then negate x else x
Prelude> myAbs 5
5
Prelude> myAbs (-5)
5
```