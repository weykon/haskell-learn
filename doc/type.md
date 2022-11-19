# Entrance of Type System

## :t maybe a usually using

I did not know whether it just a command when in CLI

and the symbol appearred as "::" mean the value typeof.

## can be explicit type declaration for value as using "::"

At primarily, 
```hs
removeNonUppercase :: [Char] -> [Char]
-- or 
removeNonUppercase :: String -> String -- because [Char] as like String
```

## how to add parameters for type of a function? 
```hs 
addThree :: Int -> Int -> Int -> Int
addThree x y z = x + y + z
```
with explain, just like ```Int,Int,Int -> Int```

Integer can contain big number rather Int not.

## big difference than other language

when 
```hs 
:t head 
-- output: 
head :: [a] -> a
```
like generaic in other language

in hs, it is to easily write general functions.

have type variables are called polymorphic.

## => called a class constraint

it is important to get understanding on it, it is a start point. 

```hs
ghci> :t (==)  
(==) :: (Eq a) => a -> a -> Bool  
```
: the equality function takes any two values that are of the same type and returns a Bool.

keyword: between two value.

(?) > (?) just like a function :  great(?,?) -> (<T>great) => great<number>(a,b) => boolean
## execute calculating a type result
```hs
5 `compare` 3
GT
```

## Show type and Read type 

Show:  to string
Read:  to its value

