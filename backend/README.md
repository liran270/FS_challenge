# Backend Developer Interview Question

## Question
Write a program that takes an integer, and returns a string representing the number in spoken English.

## Function Definition
`def convert(number: int) -> str`

## Examples
`print(convert(223))` # Two hundred twenty three
`print(convert(1000))` # One thousand
`print(convert(2147483647))`   # Two Billion, one hundred forty seven million, four hundred eighty three thousand, six hundred forty seven
`print(convert(222147483647))` # Two hundred twenty two Billion, one hundred forty seven million, four hundred eighty three thousand, six hundred forty seven

## Assumptions
* Number will not exceed MAX_INT (2147483647)
* Not need to use `and` keyword (123 --> One hundred twenty three, NOT One hundred and twenty three)
