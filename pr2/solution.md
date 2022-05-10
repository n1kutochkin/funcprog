#  Упражнение 1
```hs
length :: [a] -> Int
```
1. Принимает список аргументов любого типа
2. Параметризированный тип, поэтому может быть любой
3. Тип результата - знаковое машинное целое
4. 
```hs
Prelude> length [1,2,3,4]
4
```
```hs
Prelude> length [(1,2),(2,3),(3,4),(4,5)]
4
```
```hs
Prelude> length "hello"
5
```
# Упражнение 2

# Упражнение 3

```hs
Prelude> :t 2 + 3 == 5
2 + 3 == 5 :: Bool
Prelude>  2 + 3 == 5
True
```

# Упражнение 4
`x = 3` - присваивание литерала целочисленного

`x + 3 == 7` – функция, возвр-я логический тип

# Упражнение 5

```hs
Prelude> length [1,2,3] == 2
False
Prelude> :t length [1,2,3] == 2
length [1,2,3] == 2 :: Bool
```
Выражение корректное, будет работать ибо идет сравнение целоичисленного значения, полученного от ф-и длины списка, с другим целочисленным

```hs
length [1, 'a', 2, 'b'] 
```
Выражение некорректное, ибо список содержит разные типы значений

```hs
[1, 2.0, 3.1]
--
Prelude> :t [1, 2.0, 3.1]
[1, 2.0, 3.1] :: Fractional a => [a]
```
Корректное, получим список вещественных значений

```hs
length [1,2] + length [2,3]
```
Некорректное, получим исключение 

```hs
(3==3) && ('b' < 'a')
--
Prelude> :t (3==3) && ('b' < 'a')
(3==3) && ('b' < 'a') :: Bool
```
Корректное, ф-я, возвр-я лог.значение

```hs
(8 == 9) && 0
```
Некорректное, литерал 0 никак не может приведен для данного выражения

# Упражнение 6

```hs
Prelude> :{
Prelude| isPalindrome :: String -> Bool
Prelude| isPalindrome x = if reverse x == x then Tr
Traversable  True
Prelude| isPalindrome x = if reverse x == x then True else False
Prelude| :}
Prelude> :t isPalindrome
isPalindrome :: String -> Bool
Prelude> isPalindrome "madam"
True
Prelude> isPalindrome "mada"
False
```

# Упражнение 7
```hs
Prelude> :{
Prelude| f :: (a, b) -> (c, d) -> ((b, d), (a, c))
Prelude| f x y = let a = fst x; c = fst y; b = snd x; d = snd y in ((b, d), (a, c))
Prelude| :}
Prelude> f (1, 2) (3, 4)
((2,4),(1,3))
```