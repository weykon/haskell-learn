## first-step 

将代码放到hs文件里，终端打开所在目录运行ghci，

使用

```ghci
:l [code_file_name.hs]
```

将代码写入complie-time(run-time)中.

然后可以直接输入函数名（填入参数）运行.

## when arr concat

```hs
"hello" ++ " " ++ "world"
['w','o'] ++ ['o','t']  
```

## a way get element by index: !!
```hs
"Steve Buscemi" !! 6  
-- 'B'  
```

## basic functions 
head, tail, last, init , length, null, reverse, drop, maximum, sum, product, 

[1..20]
[2,4..20]
[3,6,..20]
[20,19..1]

## cycle 
take 10 (cycle [1,2,3])
10 items for element cycle


## | and <-
```hs
[x*2 | x <- [1..10]]
```

## more condition 
```hs 
[x*2 | x <- [1..10] , x*2>=12]
-- [12,14,16,18,20]
```

## `` with a operation 
```hs
[ x | x <- [50..100], x `mod` 7 == 3] -- which divided with 7 and remainder 3. 
-- [52,59,66,73,80,87,94]   
```

# redefined or redraw
```hs
boomBangs xs = [ if x < 10 then "BOOM!" else "BANG!" | x <- xs, odd x]  
-- boomBangs [7..13]  
-- ["BOOM!","BOOM!","BANG!","BANG!"] 
```
and The function odd returns True on an odd number and False 

# /=
```hs
[x | x <- [10..20], x/=13, x/=15, x/=19]
```

# the | with arrays
```hs 
[x * y | x <- [2,5,10], y <- [8,10,11]]
```

# what _
named a new var of length = length'
```hs
length' xs = sum [1 | _ <- xs]
```
one: whatever element from input array we predicates as a _ thing.
and they predicates to 1.
two: then sum all elements each which is 1.
so that sum the length.

--- 


# \`elem`
```hs
removeNonUppercase st = [c | c <- st, c `elem` ['A'..'Z']]
```

# zip
```hs
zip [1,2,3,4] [5,5,5,5]
-- [(1,5),(2,5),(3,5),(4,5)]
zip [1 .. 5] ["one", "two", "three", "four", "five"]  
-- [(1,"one"),(2,"two"),(3,"three"),(4,"four"),(5,"five")]  
```

# calc
```hs
let rightTriangles' = [ (a,b,c) | c <- [1..10], b <- [1..c], a <- [1..b], a^2 + b^2 == c^2, a+b+c == 24]  
-- [6,8,10]
```