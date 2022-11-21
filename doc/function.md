# Syntax in Functions


## Pattern matching 

```hs
lucky :: (Integral a) => a -> String
lucky 7 = "LUCKY NUMBER SEVER!"
lucky x = "Sorry, you're out of luck, pal!"
```

and 
```hs
sayMe :: (Integral a) => a -> String  
sayMe 1 = "One!"  
sayMe 2 = "Two!"  
sayMe 3 = "Three!"  
sayMe 4 = "Four!"  
sayMe 5 = "Five!"  
sayMe x = "Not between 1 and 5"  
```

