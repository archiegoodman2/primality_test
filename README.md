# primality_test
Simple Miller-Rabin Primality test to test if a number, n, is prime. 

The functions works probabilistically so it will not have 100% accuracy - it sacrifices this for performance, relative to manually looping through every possible number.

Will not include a full read-me because this is a short function in C# that doesn't use any libraries, frameworks or other files. Can just be ran in any IDE with .NET set up. 

Edge cases: 
0, 1 and 2. 

Testing: 
To test this, try inputting 0, 1, 2 as well as one known prime and non-prime for each of these categories:
  1. a number below 10
  2. a negative number below 10
  3. a very large positive number - to test performance
  4. a negative numebr greatly below zero

The idea for this came from a kata on CodeWars.
