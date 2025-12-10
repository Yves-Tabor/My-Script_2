# My-Script_2 

**7kyu

____________
An array is given with palindromic and non-palindromic numbers. A palindromic number is a number that is the same from a reversed order. For example 122 is not a palindromic number, but 202 is one.

Your task is to write a function that returns an array with only 1s and 0s, where all palindromic numbers are replaced with a 1 and all non-palindromic numbers are replaced with a 0.

For example:

[101, 2, 85, 33, 14014]  ==>  [1, 1, 0, 1, 0]
[45, 21, 303, 56]        ==>  [0, 0, 1, 0]

Link: https://www.codewars.com/kata/5838a66eaed8c259df000003/train/javascript/68af10b57dfdd33e710e3443
Solution: 

function convertPalindromes (arr) {
    const test = (item) =>{
        const a = String(item);
        const rev = a.split("").reverse().join("");
        if(a.includes(rev)){
            return 1;
        }else{
            return Number("0");
        }
    } 
    return arr.map(item=> test(item));
}
