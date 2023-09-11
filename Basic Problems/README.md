## Loops,Functions & Math Problems

## Question-1

`Given two non-negative integers low and high. Return the count of odd numbers between low and high (inclusive).`

```
var countOdds = function(low, high) {
    let odd = 0;
    for (let i = low; i <= high; i++) {
        if (i % 2 != 0) {
            odd++;
        }
    }
    return odd;
};

console.log(countOdds(3, 7));
```

## Question-2

`Given an integer n, return a string array answer (1-indexed) where:`
`answer[i] == "FizzBuzz" if i is divisible by 3 and 5.`
`answer[i] == "Fizz" if i is divisible by 3.`
`answer[i] == "Buzz" if i is divisible by 5.`
`answer[i] == i (as a string) if none of the above conditions are true.`

```
var fizzBuzz = function(n) {
    let a=[];
    for(let i=1;i<=n;i++){
        if(i%3===0 && i%5===0){
            a.push("FizzBuzz");
        }
        else if(i%3===0){
            a.push("Fizz");
        }
        else if(i%5===0){
            a.push("Buzz")
        }
        else{
            a.push(i.toString())
        }
    }
    return a;
};
console.log(fizzBuzz(5))
```

## Question-3

`Given an integer n, return true if it is a power of two. Otherwise, return false.`

`An integer n is a power of two, if there exists an integer x such that n == 2x.`

```
var isPowerOfTwo = function(n) {
    if(n<1){
        return false;
    }
    else{
        return (n & (n-1))===0;
    }
};
console.log(isPowerOfTwo(3));
```

## Question-4

`Given a non-negative integer x, return the square root of x rounded down to the nearest integer. The returned integer should be non-negative as well.`

```
var mySqrt = function(x) {
    let start=1;
    while(start*start<=x){
        start++;
    }
    return start-1;
};
console.log(mySqrt(15))
```
