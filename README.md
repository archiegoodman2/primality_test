# primality_test
Simple Miller-Rabin Primality test to test if an integer, n, is prime. 

The functions works probabilistically so it will not have 100% accuracy - it sacrifices this for performance, relative to manually looping through every possible number.

Will not include a full read-me because this is a short function in C# that doesn't use any libraries, frameworks or other files. Can just be ran in any IDE with .NET set up. 

**The idea for this was inspired by the tutorial:** https://youtu.be/-BWTS_1Nxao?si=F4MIpK2uZgEzi0pK   The mathematics of a Mille Rabin test can be found on this video.
However, this was heavily modified as his tutorial was in Python, and the two languages do not work exactly the same. 

**Edge cases:** 
0, 1 2 and perhaps 3.

**Testing: **
To test this, try inputting 0, 1, 2 as well as one known prime and non-prime for each of these categories:
  1. a number below 10
  2. a very large positive number - to test performance

The idea for this came from a kata on CodeWars.


**To improve next time**: perhaps use more bitwise operators to improve speed, and check use of random function to make it more cryptograpphically secure. consider other libraries to import that may contain rand int generator. time-efficiency analysis also required.

According to ChatGPT, we could use this bit manipulation logic, instead, for the first method:

private static bool SingleTest(BigInteger n, BigInteger a)
    {
        BigInteger nMinus1 = n - 1;
        BigInteger exp = nMinus1;
        int trailingZeros = 0;

        // Extract the number of trailing zeros in nMinus1
        while (exp.IsEven)
        {
            exp >>= 1;
            trailingZeros++;
        }
  ...

So I will look into what trailing zeroes are. 
