# protoscan
* Prototype Pollution Scanner made in Golang, it was actually made by @tomnomnom in NahamCon2021 https://www.youtube.com/watch?v=Gv1nK6Wj8qM
* I just made it for fun and added some extra features 

# Installation:

`go get github.com/KathanP19/protoscan`

# Usage:
```

         _____           _        _____                 
        |  __ \         | |      / ____|                
        | |__) _ __ ___ | |_ ___| (___   ___ __ _ _ __  
        |  ___| '__/ _ \| __/ _ \\___ \ / __/ _  | '_ \ 
        | |   | | | (_) | || (_) ____) | (_| (_| | | | |
        |_|   |_|  \___/ \__\___|_____/ \___\__,_|_| |_|

                                -@KathanP19

Usage of protoscan:
  -c int
        Set Concurrency  (default 10)
  -o string
        Save Result to OutputFile
  -u    Scan Urls 
```
* If you want to test then you can use the testurls.txt
`cat testurls.txt | protoscan`

* If you want to scan urls `For Example: http://example.com/?page=some` then use `-u` option.
`cat testurls.txt | protoscan -u`

# Payloads Used:
* By Default it will append `?__proto__[protoscan]=protoscan` to the `https://example.com` so you can directly STDIN the output of Httpx or some other tool after you check that domain is live.
```
https://example.com/?__proto__[protoscan]=protoscan
```
* When `-u` is used it will append `&__proto__[protoscan]=protoscan` to the url 
```
https://example.com/?page=some&__proto__[protoscan]=protoscan`
```

# More Info:
If you want to learn prototype pollution then you can check this repo.
- https://github.com/BlackFan/client-side-prototype-pollution

# TODO:
- [ ] Add more Payload Support. 
