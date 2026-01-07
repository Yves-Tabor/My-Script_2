


# My-Script_2 

**7kyu
____________
Deoxyribonucleic acid (DNA) is a chemical found in the nucleus of cells and carries the "instructions" for the development and functioning of living organisms.

If you want to know more: http://en.wikipedia.org/wiki/DNA

In DNA strings, symbols "A" and "T" are complements of each other, as "C" and "G". Your function receives one side of the DNA (string, except for Haskell); you need to return the other complementary side. DNA strand is never empty or there is no DNA at all (again, except for Haskell).

More similar exercise are found here: http://rosalind.info/problems/list-view/ (source)

Example: (input --> output)

"ATTGC" --> "TAACG"
"GTAT" --> "CATA"

Solution:
function dnaStrand(dna){
  return dna.replace(/A/g, 'X')
    .replace(/T/g, 'A')
    .replace(/X/g, 'T')
    .replace(/C/g, 'Y')
    .replace(/G/g, 'C')
    .replace(/Y/g, 'G');

}
________________________

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
